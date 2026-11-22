# Third-Party Notices

Moby には以下のサードパーティ製ソフトウェアが含まれています。各ソフトウェアの著作権はそれぞれの権利者に帰属し、各ライセンスに従って配布されています。

許諾文の全文は、配布の zip の `licenses/` フォルダーに入っています。

| ファイル | 中身 |
|---|---|
| `licenses/GPL-3.0.txt` | GNU General Public License version 3 の本文（FFmpeg・ffmpeg-static） |
| `licenses/FFmpeg/SOURCE.txt` | FFmpeg と外部ライブラリの版・commit・ソースの入手先 |
| `licenses/FFmpeg/BUILD-README.txt` | 同梱の FFmpeg のビルドの設定 |
| `licenses/THIRD_PARTY_LICENSES.txt` | 実行ファイルに含まれる npm パッケージすべての許諾文 |
| `licenses/LICENSE.electron.txt` | Electron の許諾文 |
| `licenses/LICENSES.chromium.html` | Chromium（Electron に含まれる）とその部品の許諾文 |

## FFmpeg（GPL v3）

- 同梱のプログラム: `ffmpeg.exe`・`ffprobe.exe`
- 版: FFmpeg 6.1.1 essentials build by www.gyan.dev（`6.1.1-essentials_build-www.gyan.dev`、FFmpeg のタグ `n6.1.1`、commit `e38092ef9395d7049f871ef4d5411eb410e283e0`）。2 つとも同じビルドです
  - `ffmpeg.exe` は npm パッケージ `ffmpeg-static` 5.3.0 が取得したもの、`ffprobe.exe` は同じビルドの zip（https://github.com/GyanD/codexffmpeg/releases/download/6.1.1/ffmpeg-6.1.1-essentials_build.zip ）から取り出したものです
- ライセンス: GNU General Public License version 3（`--enable-gpl --enable-version3`。libx264・libx265 などの GPL のライブラリを含みます）
- FFmpeg は Moby 本体とは独立した別プログラムとして同梱され、別プロセスとして呼び出されます
- 対応するソース: https://github.com/n-yoshida-polaris/moby-release/releases/tag/ffmpeg-6.1.1-sources に、FFmpeg 本体と外部ライブラリのソースを置いています。各プロジェクトの配布元は `licenses/FFmpeg/SOURCE.txt` にあります
  - FFmpeg 6.1.1: https://ffmpeg.org/releases/ffmpeg-6.1.1.tar.xz
  - ビルド元: https://www.gyan.dev/ffmpeg/builds/ （ビルドのスクリプト: https://github.com/m-ab-s/media-autobuild_suite ）
- GPL v3 全文: `licenses/GPL-3.0.txt`（https://www.gnu.org/licenses/gpl-3.0.html ）

## Electron・Chromium

- Electron 34.5.8（MIT）: `licenses/LICENSE.electron.txt`。ソース: https://github.com/electron/electron
- Chromium と、その部品（動画の再生に使う `ffmpeg.dll`（LGPL 2.1）を含む）: `licenses/LICENSES.chromium.html`

## npm パッケージ

実行ファイルには、下の直接の依存と、その先の依存を合わせて 200 個あまりの npm パッケージが含まれています。すべての名前・版・許諾文は `licenses/THIRD_PARTY_LICENSES.txt` にあります（ビルドのたびに作り直します）。

| パッケージ | バージョン | ライセンス |
|---|---|---|
| express | 5.2.1 | MIT |
| fluent-ffmpeg | 2.1.3 | MIT |
| ffmpeg-static | 5.3.0 | GPL-3.0-or-later |
| dotenv | 17.3.1 | BSD-2-Clause |
| sqlite3 | 5.1.7 | BSD-3-Clause（同梱の SQLite はパブリックドメイン） |
| flv.js | 1.6.2 | Apache-2.0 |
| video.js | 8.23.7 | Apache-2.0 |

その先の依存のライセンスは、MIT・ISC・Apache-2.0・BSD-2-Clause・BSD-3-Clause などです。
