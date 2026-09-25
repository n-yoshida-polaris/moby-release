# Third-Party Notices

Moby には以下のサードパーティ製ソフトウェアが含まれています。各ソフトウェアの著作権はそれぞれの権利者に帰属し、各ライセンスに従って配布されています。

## FFmpeg（GPL v3）

- 同梱バイナリ: `ffmpeg.exe`（`ffmpeg-static` 5.3.0 経由、FFmpeg 6.1.1 essentials build by www.gyan.dev）/ `ffprobe.exe`（`ffprobe-static` 3.1.0 経由）
- ライセンス: GNU General Public License version 3
- FFmpeg は Moby 本体とは独立した別プログラムとして同梱され、別プロセスとして呼び出されます
- ソースコード: https://ffmpeg.org/download.html / ビルド元: https://www.gyan.dev/ffmpeg/builds/
- GPL v3 全文: https://www.gnu.org/licenses/gpl-3.0.html

## npm パッケージ

| パッケージ | バージョン | ライセンス |
|---|---|---|
| Electron | 34.5.8 | MIT |
| express | 5.2.1 | MIT |
| chokidar | 5.0.0 | MIT |
| fluent-ffmpeg | 2.1.3 | MIT |
| ffmpeg-static | 5.3.0 | GPL-3.0-or-later |
| ffprobe-static | 3.1.0 | MIT |
| dotenv | 17.3.1 | BSD-2-Clause |
| sqlite3 | 5.1.7 | BSD-3-Clause |
| flv.js | 1.6.2 | Apache-2.0 |
| video.js | 8.23.7 | Apache-2.0 |

各パッケージのライセンス全文は、それぞれのパッケージに同梱されている LICENSE ファイルを参照してください。
