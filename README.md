# APDL-Power-Module-Thermal-Mechanical-Analysis-Scripts
APDL Power Module Thermal–Mechanical Analysis Scripts
APDL パワーモジュール熱・機械解析スクリプト

## Overview / 概要
This repository contains APDL automation scripts for thermal–mechanical analysis of
power module structures including multiple chips, ,DBC substrates, solder layers, resin encapsulation, and busbars.
All geometric dimensions are fully parameterized
The scripts are fully parameterized and designed for large-scale batch execution.

本リポジトリは、IGBT チップ、チップパラ数、DBC 基板、はんだ層、樹脂封止、バスバーなどを含む
パワーモジュール構造の熱・機械解析を自動化する APDL スクリプトをまとめたものです。
全ての寸法をパラメータで指定可能
完全パラメトリック化されており、大規模バッチ解析に対応しています。

## Features / 特徴
- Fully parameterized APDL model generation
- Automated mesh sizing for solder, chip, resin, and copper
- PCT/TCT stress analysis automation
- Suitable for batch execution and optimization workflows (e.g., ModeFrontier)

- 完全パラメトリック化された APDL モデル生成
- はんだ・チップ・樹脂・銅の自動メッシュ設定
- PCT/TCT 応力解析の自動化
- ModeFrontier 等の最適化ツールによるバッチ実行に対応

## Model Description / モデル概要
The scripts generate a multi-layer structure consisting of:
- opper plates (upper/lower DBC)
- Ceramic substrates
- IGBT chips
- Solder layers (die attach, emitter, spacer, busbar)
- Resin encapsulation
- Signal pins and busbar islands
- Mesh density and geometry are automatically computed from user-defined parameters.

本スクリプトは以下の多層構造を自動生成します：
- 上下 DBC の銅板
- セラミック基板
- IGBT チップ
- はんだ層（ダイ・エミッタ・スペーサ・バス）
- 樹脂封止
- 信号ピン・バス島
- メッシュ粗さや形状は、ユーザーが設定したパラメータから自動計算されます。

## How to Use / 使用方法
Launch ANSYS Mechanical APDL
Place material files under material/
Run scripts in src/
Modify parameters at the beginning of each script
Use batch mode for long thermal–mechanical simulations

ANSYS Mechanical APDL を起動
material/ に材料データを配置
src/ 内のスクリプトを実行
冒頭のパラメータを編集してモデルを調整
長時間の熱・機械解析はバッチモード推奨

## Examples / 実行例
examples/simple_solder_block.mac  
→ はんだブロックの最小モデル

examples/dbc_stack.mac  
→ DBC 多層構造の生成例

## Background / 背景
These scripts are based on real industrial workflows and include
practical adjustments such as:
Solder fillet angle tuning
Contact failure avoidance
Mesh stabilization for large solder areas
Parameterized DBC geometry
Resin fine-mesh region control

本スクリプトは実務での試行錯誤を反映しており、以下の調整を含みます：
はんだフィレット角度の調整
接触破綻の回避
大面積はんだのメッシュ安定化
DBC 形状のパラメトリック化
樹脂細メッシュ領域の自動設定

## License / ライセンス
MIT License（任意で変更可）

## Contact / 連絡先
If you have questions or requests, feel free to open an Issue.
質問や要望があれば、Issue を作成してください。
