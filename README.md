# シフトスケジューラー

このプログラムは、特定の時間帯で必要な人員を確保するために、利用可能な個人のスケジュールからシフトを自動的に作成します。貪欲法を用いて初期スケジュールを生成し、その後山登り法を用いて解を改善します。

## 機能

- アンケートデータから利用可能な時間帯を読み込む。
- 貪欲法による初期シフトスケジュールの作成。
- 山登り法によるシフトスケジュールの最適化（現在は未実装）。
- スケジュールデータのCSV出力。

## システム要件

- Python 3.7 以上
- pandas ライブラリ
- datetime ライブラリ

## セットアップ

以下の手順に従って環境をセットアップしてください。

1. Pythonをインストールします（未インストールの場合）。[Python公式サイト](https://www.python.org/downloads/)からダウンロードできます。
2. 必要なライブラリをインストールします：
    ```bash
    pip install pandas
    ```

## 使用方法

1. アンケート結果をCSVファイル (`chouseisan.csv`) として保存し、プログラムと同じディレクトリに配置します。
2. CSVファイルの1行目にはヘッダーを、2行目以降に各人物の利用可能な時間帯を「◯」としてマークし、最終行にコメントを記述してください。
3. コマンドラインまたはターミナルからプログラムを実行します：
    ```bash
    python main.py
    ```
4. 必要な人数を入力します。
5. プログラムがCSVファイルを生成し、指定されたシフトスケジュールが出力されます。

## CSVファイル形式

[調整さん](https://chouseisan.com/)から出力できるファイルをそのまま利用できます。
**出欠表をダウンロードする**から、
- 文字コードをUTF-8
- 行と列の設定を標準
  
に設定後、ダウンロードしてください。

## 注意事項

現在、山登り法による最適化は実装されていません。初期の貪欲法によるスケジュール生成のみが機能します。
