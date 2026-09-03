# SQLite Installation and Setup on Windows

## Problem

When running:

```powershell
sqlite3 data.db
```

You may see:

```text
sqlite3 : The term 'sqlite3' is not recognized as the name of a cmdlet, function, script file, or operable program.
```

This error means that Windows cannot find `sqlite3.exe`.

---

## Step 1: Download SQLite

1. Visit the SQLite download page:

   * https://www.sqlite.org/download.html

2. Download:

   * `sqlite-tools-win-x64-*.zip`

3. Extract the ZIP file.

Example location:

```text
C:\sqlite
```

After extraction, you should see:

```text
sqlite3.exe
sqldiff.exe
sqlite_analyzer.exe
```

---

## Step 2: Verify SQLite Works

Open PowerShell and navigate to the SQLite folder:

```powershell
cd C:\sqlite
```

Run:

```powershell
.\sqlite3.exe
```

If successful, you will see:

```text
SQLite version x.x.x
Enter ".help" for usage hints.
sqlite>
```

Exit SQLite:

```sql
.quit
```

---

## Step 3: Add SQLite to Windows PATH

To use SQLite from any folder, add the SQLite directory to the PATH environment variable.

### Instructions

1. Press **Windows Key**
2. Search for **Environment Variables**
3. Open **Edit the system environment variables**
4. Click **Environment Variables**
5. Under **User Variables**, select **Path**
6. Click **Edit**
7. Click **New**
8. Add your SQLite folder path

Example:

```text
C:\sqlite
```

9. Click **OK** on all windows

---

## Step 4: Restart Terminal

Close all PowerShell or CMD windows.

Open a new terminal and verify installation:

```powershell
sqlite3 --version
```

You should see the installed SQLite version.

---

## Step 5: Create a Database Anywhere

Navigate to any project folder:

```powershell
cd D:\Projects\FlaskApp
```

Create or open a database:

```powershell
sqlite3 data.db
```

SQLite will automatically create `data.db` if it does not already exist.

---

## Verify PATH Configuration

Run:

```powershell
where sqlite3
```

Expected output:

```text
C:\sqlite\sqlite3.exe
```

If you see the path to `sqlite3.exe`, the configuration is successful.

---

## Useful SQLite Commands

List all tables:

```sql
.tables
```

Create a table:

```sql
CREATE TABLE users (
    id INTEGER PRIMARY KEY,
    name TEXT
);
```

Exit SQLite:

```sql
.quit
```

---

## Notes

* `.\sqlite3.exe` means "run sqlite3.exe from the current folder."
* After adding SQLite to PATH, you can simply use:

```powershell
sqlite3 data.db
```

from any directory on your computer.
