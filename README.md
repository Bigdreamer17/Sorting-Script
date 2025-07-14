# 📁 File Sorter Script

A simple and customizable Bash script to automatically organize files in a directory based on their type. It groups common file types into folders like `E-Books`, `Pics`, `Vids`, `Audio`, etc., making your folders cleaner and easier to navigate.

## 📦 Features

- Sorts files into organized folders based on their extensions:
  - 📚 **E-Books**: `.pdf`, `.epub`, `.txt`, `.csv`, `.docx`, `.doc`
  - 🖼️ **Images**: `.png`, `.jpeg`, `.jpg`, `.JPG`, `.svg`
  - 🎬 **Videos**: `.mp4`, `.mkv`, `.webm`
  - 🔊 **Audio**: `.mp4`, `.m4a`
  - 📊 **Presentations**: `.pptx`, `.xlsx`, `.xls`
  - 🗜️ **Zipped Files**: `.zip`, `.tar.xz`, `.rpm`, `.jar`, `.bz2`, `.deb`
  - 🧾 **JSON Files**: `.json`
- Customizable modes: run all at once or sort specific types only
- Works on any given directory (default: current directory)
- Includes helpful `-h` flag for usage instructions


## 🧪 Usage

```bash
./sort [OPTIONS]
```
## 🔧 Options
| Option      | Description                                                                                                                              |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| `-d <dir>`  | Target directory to sort. If omitted, defaults to the current directory (`.`).                                                           |
| `-m <mode>` | What to sort. Options include:<br>• `all`<br>• `audio`<br>• `ebook`<br>• `video`<br>• `presentation`<br>• `zip`<br>• `json`<br>• `image` |
| `-h`        | Show help message and exit.                                                                                                              |

## 📂 Example Commands
### Sort everything in a specific folder:
```bash
./sort -d ~/Downloads
```

### Sort only images in the current directory:
```bash
./sort -m image
```

### Sort only zip files in your Desktop:
```bash
./sort -d ~/Desktop -m zip
```

🧠 Notes
- If the target folder (e.g., Pics, E-Books) doesn’t exist, the script will create it.

- Files with spaces in names are properly handled.

- The script does not currently recurse into subdirectories.

- Files are moved, not copied. Be careful when running on important directories.

- Duplicate file names may be overwritten if they already exist in the destination folder.

## 🌐 Make it Global
#### To use the script from anywhere:
1. Make it executable:
   ```bash
   chmod +x sort
   ```
2. Move it to a directory in your $PATH:
   ```bash
   sudo mv sort /usr/local/bin/
   ```
3. Now you can use sort globally:
   ```bash
   sort -d ~/Downloads -m all
   ```
