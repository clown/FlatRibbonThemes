# FlatRibbonThemes

FlatRibbonThemes は、Microsoft Ribbon for WPF のデザインをカスタマイズしやすくするために、各種効果（グラデーション等）を無効にするためのプロジェクトです。

## Features

FlatRibbonThemes の *.xaml は、以下の色、効果を修正します。括弧内で表記している記号は、オリジナルの Generic.xaml で定義されているキー名を表します。

* 共通色
    * &#203 ... #FF9E9E9E -> SystemColors.GrayTextColor
    * &#227 ... #80FFFFFF -> SystemColors.ControlColor
    * &#229 ... #B8FFFFFF -> SystemColors.ControlLightColor
    * &#263 ... #EEFFFFFF -> SystemColors.WindowColor
* Ribbon
    * BorderBrush (&#204)、および Background (&#205) を修正
* RibbonTab
    * Background に指定した色が反映されるように修正
    * RibbonTabHeader は未修整なので、RibbonTabHeader.CheckedBackground を適宜指定する事
* RibbonGroup
    * マウスオーバ時の背景色 (&#278, &#279, &#284) を修正
    * Header を非表示に修正
* RibbonApplicationMenu
    * ボタンの背景色 (&#216) を修正
    * ボタンの上部枠線の効果 (&#217) は未修整
    * Header, MainPane, Footer の枠線 (&#227)、および背景色 (&#218, &#220, &#229) を修正
    * PopupBorder の BorderBrush, Background をそれぞれ RibbonApplicationMenu の FocusedBorderBrush, FocusedBackground に対応
* RibbonMenuItem
    * Background (&#239) を修正
    * Foreground を SystemColors.MenuTextBrush に修正
    * SideBarBorder の BorderBrush, Background をそれぞれ Ribbon.CheckdedBorderBrush, Ribbon.CheckedBackground に対応
    * SideBarOverlay.Background (&#228) を修正
* RibbonGalleryItem
    * Foreground を SystemColors.MenuTextBrush に修正
* RibbonSplitButton
    * MouseOver 時の背景色 (&#295) を修正
* RibbonTextBox
    * Foreground を SystemColors.WindowTextBrush に修正
* RibbonCheckBox
    * CheckMark を SystemColors.WindowTextBrush に修正
* RibbonComboBox
    * Foreground, Arrow を SystemColors.WindowTextBrush に修正
    * TODO: Label の色も SystemColors.WindowTextBrush に固定化されているので、Ribbon.Foreground 辺りを適用する
* RibbonToolTip
    * BorderBrush, Background を修正

## Installation

1. [Microsoft Ribbon for WPF](http://www.microsoft.com/en-us/download/details.aspx?id=11877 "Microsoft Ribbon for WPF") から Microsoft Ribbon for WPF Source and Samples.msi をダウンロードし、インストールします。尚、このプロジェクト修正時のバージョンは、Version: 4.0.0.11019, Date published: 10/22/2010 となっています。
2. インストール先（デフォルトでは、C:\Program Files\Microsoft Ribbon for WPF）にある MicrosoftRibbonForWPFSourceAndSamples.zip と言う圧縮ファイルを適当なフォルダに展開します。
3. 展開先の RibbonControlsLibrary\v3.5\Themes\Generic.xaml、または、RibbonControlsLibrary\v4.0\Themes\Generic.xaml をこのプロジェクトの該当バージョンの Generic.xaml で置き換えます。
4. Visual Studio でビルドを実行し、RibbonControlsLibrary プロジェクトが生成した RibbonControlsLibrary.dll を標準の dll の代わりに使用します。

## History

### 2013-05-03
* RibbonApplicationMenu のポップアップメニューの色をカスタマイズ可能なように修正しました。
* RibbonGroup の Header を非表示に修正しました。
* RibbonMenuItem の SideBarBorder の色を修正しました。

### 2013-05-02
* 修正方法を変更しました（各コンポーネントを直接変更する代わりに、できる限り定義されているキーを修正）。
* RibbonTextBox, RibbonCheckBox, RibbonComboBox 等、白背景 (WidnowColor) を強制するコンポーネントの枠線、背景色を修正しました。
* RibbonMenuItem, RibbonGalleryItem の Foreground を MenuTextColor に修正しました。
* RibbonToolTip の枠線、および背景色を修正しました。

### 2013-04-25
* RibbonMenuItem の背景色をリセットしました。

### 2013-04-19
* Ribbon.Background, RibbonTabHeader.CheckedBackground のグラデーション効果を削除しました。
* RibbonGroup に関して、PART_HotBackground.Background, RibbonToggleButton.LabelBorder.Background, RibbonToggleButton.ImageOuterBorder.Background, PART_Popup.PART_HotBackground.Background のグラデーション、および強調効果を削除しました。
* RibbonToolTip.InnerBorder.Background のグラデーション効果を削除しました。
* RibbonApplicationMenu に関わるグラデーション、および強調効果を削除しました。
