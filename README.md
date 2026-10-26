# WBFS_Manager
This application basically provides a GUI for working with hard disk drives that have been formatted to the WBFS file system.

## Test release

The current **[Windows test pre-release](https://github.com/sh1bot/WBFS_Manager/releases/tag/test-839a5f8)** contains downloadable ZIPs for x86, x64 and ARM64, plus SHA-256 checksums.

These builds have passed automated builds and startup checks, and users have confirmed that all three download and launch. Disk-writing features and channel creation are not fully validated. The release is labelled **pre-release**, not stable.

Future test releases can be published by committing to `master` with `[publish-test]` in the commit message. The GitHub Actions workflow builds all three architectures, verifies the package manifests, and publishes a tagged pre-release with downloadable ZIP assets.

## Development downloads

The current [GitHub Actions builds](https://github.com/sh1bot/WBFS_Manager/actions/workflows/windows-build.yml) provide separate x86, x64, and experimental ARM64 diagnostic ZIPs. These are **not official releases** and should be extracted before use.

- **x86:** Windows .NET Framework 4.8, paired with a source-built x86 WBFS native wrapper. An earlier x86 package was manually launch-tested.
- **x64:** Windows .NET Framework 4.8, paired with the source-built x64 native wrapper. CI-compiled, not yet user-tested.
- **ARM64:** Windows 11 ARM64 with .NET Framework 4.8.1 and a native ARM64 WBFS wrapper. CI verifies the managed assembly, native DLL loading, and architecture; GUI and disk operations are not yet user-tested.

Current packages include SharpCompress for RAR ISO imports in place of obsolete UnRAR native DLLs. The legacy ChannelCreation and bannerExtractionWrapper components are **not yet packaged**, so channel creation and related functionality may not work. The OpenSSL 3 native rebuild remains experimental. Do not use unverified builds for disk formatting or writing without independent backups and testing.

The ZIPs include SHA256SUMS.txt for verifying the packaged files. GitHub Actions also records the artifact ZIP digest.

Downloads

Features
Listing of games with titles, sizes and codes.
Drag-and-drop support for adding multiple files at once to the WBFS drive.
Easy to use interface which also reports available, total and used disk space at a glance.
Batch processing of multiple ISOs.
Rename discs on the WBFS drive.
Multilingual support
French, courtesy of TheCrach
Italian and Perugino, courtesty of cerocca
German, courtesy of BarbaxX
Spanish, courtesy of dgtor
Dutch, courtesy of villadelfia
Chinese (Traditional), courtesy of IvanChen
Homebrew Channel entry creation
Indirect Drive-To-Drive transferring and cloning
Automatic RAR archive extraction
Batch extraction and deletion
Exporting list of games on drive to a .CSV
Ability to use more than one cover directory
Channel Creation (NEW)

Requirements
Current CI binaries: .NET Framework 4.8 (x86/x64), or .NET Framework 4.8.1 on Windows 11 ARM64. The original installer and its .NET Framework 3.5 requirement refer to the historical release.

Instructions
Install using setup.
Plug in the hard drive or USB stick.
Run the application.
Choose the correct drive letter.
Click Load. (If you haven't already formatted the disk to WBFS, you can do that by clicking Format).
You should now see any backups on the drive on the left hand side.
You can drag and drop ISO files from Windows Explorer onto the right hand side or you can click the browse button.
Click the Add to Drive button to copy them over to the WBFS drive.
Enjoy!

Completed Future Plans
Using libwbfs directly to achieve greater flexiblity.
Use a separate worker thread to improve responsiveness when doing IO operations.
UnRar functionality to automatically UnRar files and add the iso to the WBFS drive.

Remaining Future Plans (Cancelled)
ISO library
Additional info from ISO (Game image shown in Disc Channel,...)

DISCLAIMER (Borrowed from Waninkoko, hopefully he won't mind )
THIS APPLICATION COMES WITH NO WARRANTY AT ALL, NEITHER EXPRESS NOR IMPLIED.
I DO NOT TAKE ANY RESPONSIBILITY FOR ANY DAMAGE TO YOUR WII CONSOLE
BECAUSE OF IMPROPER USAGE OF THIS SOFTWARE.
