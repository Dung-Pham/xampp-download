## 1. Fix error xampp: "MySQL shutdown unexpectedly"

**Step 1** Rename the folder C:\xampp\mysql\data to C:\xampp\mysql\data_bkp (you can use any name).

**Step 2** Create a new folder, C:\xampp\mysql\data.

**Step 3** Copy the content that resides in mysql\backup to the new mysql\data folder.

**Step 4** Copy all your database folders that are in mysql\data_bkp to mysql\data (skipping the mysql, performance_schema, and phpmyadmin folders from mysql\data_bkp).

**Important note:** Please do not replace the existing files while pasting (click skip for these files)

Enter image description here

**Step 5** Finally copy the ibdata1 file from mysql\data_bkp and replace it inside the mysql\data folder.

**Step 6** Start MySQL from XAMPP control panel.

And, it's done. No databases were lost, no ports changed, no run as administrator, no force recovery, no kill mysqld process, no restoring from previous versions, and no more errors.

---
## 2. Fix error : "WILL NOT start without the configured ports free!"
**Step 1** Xác định ứng dụng chiếm giữ port 443:
Mở Command Prompt dưới quyền Administrator.
Chạy lệnh sau để xác định ứng dụng nào đang chiếm giữ port 443:
```bash
netstat -ano | findstr :443
```
Lệnh này sẽ hiển thị PID (Process ID) của ứng dụng đang sử dụng port 443.

**Step 2** Dừng ứng dụng chiếm giữ port 443:
Sau khi xác định PID, bạn có thể dừng ứng dụng đó bằng cách chạy lệnh sau trong Command Prompt:
```bash 
taskkill /PID <PID> /F
```
Thay <PID> bằng PID của ứng dụng đã xác định.

---
## 3. Link to download git LFS: 

https://git-lfs.com/


***Install***
git LFS install

C:\Users\Admin>git lfs install
Git LFS initialized.


Admin@DungPh?m MINGW64 /d/xampp-download (main)
$ git add .gitattributes

Admin@DungPh?m MINGW64 /d/xampp-download (main)
$ git add . xampp-windows-x64-8.0.30-0-VS16-installer.exe

Admin@DungPh?m MINGW64 /d/xampp-download (main)
$ git commit -m "add xampp with git lfs'
> ^C

Admin@DungPh?m MINGW64 /d/xampp-download (main)
$ git commit -m "add xampp with git lfs"
[main 53deb5d] add xampp with git lfs
 2 files changed, 2 insertions(+)

Admin@DungPh?m MINGW64 /d/xampp-download (main)
$ git push
Uploading LFS objects: 100% (2/2), 302 MB | 2.9 MB/s, done.
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 8 threads
Compressing objects: 100% (15/15), done.
client_loop: send disconnect: Connection reset by peer
send-pack: unexpected disconnect while reading sideband packet
fatal: sha1 file '<stdout>' write error: Broken pipe
fatal: the remote end hung up unexpected






Admin@DungPh?m MINGW64 /d/git LFS file/xampp-download (main)
$ git lfs track "*.exe"
Tracking "*.exe"

Admin@DungPh?m MINGW64 /d/git LFS file/xampp-download (main)
$ git lfs track "*.rar"
Tracking "*.rar"

Admin@DungPh?m MINGW64 /d/git LFS file/xampp-download (main)
$ git add .gitattributes

Admin@DungPh?m MINGW64 /d/git LFS file/xampp-download (main)
$ git commit -m "add xampp with git lfs"
[main (root-commit) 5ae7394] add xampp with git lfs
 1 file changed, 2 insertions(+)
 create mode 100644 .gitattributes

Admin@DungPh?m MINGW64 /d/git LFS file/xampp-download (main)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 283 bytes | 283.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:Dung-Pham/xampp-download.git
 * [new branch]      main -> main

Admin@DungPh?m MINGW64 /d/git LFS file/xampp-download (main)
$ git add .

Admin@DungPh?m MINGW64 /d/git LFS file/xampp-download (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   xampp-windows-x64-8.0.30-0-VS16-installer.rar


Admin@DungPh?m MINGW64 /d/git LFS file/xampp-download (main)
$ git commit -m "push xampp with git lfs"
[main 7ceff51] push xampp with git lfs
 1 file changed, 3 insertions(+)
 create mode 100644 xampp-windows-x64-8.0.30-0-VS16-installer.rar

Admin@DungPh?m MINGW64 /d/git LFS file/xampp-download (main)
$ git push
Uploading LFS objects: 100% (1/1), 150 MB | 3.9 MB/s, done.
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 454 bytes | 454.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:Dung-Pham/xampp-download.git
   5ae7394..7ceff51  main -> main

Admin@DungPh?m MINGW64 /d/git LFS file/xampp-download (main)
$



