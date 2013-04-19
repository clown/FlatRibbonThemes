# FlatRibbonThemes

FlatRibbonThemes は、Microsoft Ribbon for WPF のデザインをカスタマイズしやすくするために、各種効果（グラデーション等）を無効にするためのプロジェクトです。

## Features

FlatRibbonThemes の *.xaml は、以下の効果を無効にします。

* Ribbon
    * Background のグラデーション
* RibbonTabHeader
    * CheckedBackground （タブの選択状態時）のグラデーション
* RibbonGroup
    * PART_HotBackground.Background （グループへのマウスオーバ時）のグラデーション
    * RibbonToggleButton （内容省略時に表示されるグループ用ボタン）の LabelBorder.Background, ボタン押下時 (IsChecked) の ImageOuterBorder.Background, LabelBorder.Background のグラデーション、または強調効果
    * PART_Popup （RibbonToggleButton を押下時に表示されるポップアップ）の PART_HotBackground.Background のグラデーション

## Installation

1. [Microsoft Ribbon for WPF](http://www.microsoft.com/en-us/download/details.aspx?id=11877 "Microsoft Ribbon for WPF") から Microsoft Ribbon for WPF Source and Samples.msi をダウンロードし、インストールします。尚、このプロジェクト修正時のバージョンは、Version: 4.0.0.11019, Date published: 10/22/2010 となっています。
2. インストール先（デフォルトでは、C:\Program Files\Microsoft Ribbon for WPF）にある MicrosoftRibbonForWPFSourceAndSamples.zip と言う圧縮ファイルを適当なフォルダに展開します。
3. 展開先の RibbonControlsLibrary\v3.5\Themes\Generic.xaml、または、RibbonControlsLibrary\v4.0\Themes\Generic.xaml をこのプロジェクトの該当バージョンの Generic.xaml で置き換えます。
4. Visual Studio でビルドを実行し、RibbonControlsLibrary プロジェクトが生成した RibbonControlsLibrary.dll を標準の dll の代わりに使用します。

## History

### 2013-04-19
* Ribbon.Background, RibbonTabHeader.CheckedBackground のグラデーション効果を削除しました。
* RibbonGroup に関して、PART_HotBackground.Background, RibbonToggleButton.LabelBorder.Background, RibbonToggleButton.ImageOuterBorder.Background, PART_Popup.PART_HotBackground.Background のグラデーション、または強調効果を削除しました。
