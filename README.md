# oracle-format

> PL/SQL formatter using SQLcl

Inspired by [atom-oracle-format](https://github.com/diesire/atom-oracle-format) and [SQLcl – Setting Up the Formatter](https://www.thatjeffsmith.com/archive/2017/03/sqlcl-setting-up-the-formatter/).

## Usage

Works with `Format Document`, `Format Selection` commands and `editor.formatOnSave` setting for `plsql` and `oraclesql`  language files.

## Configuration

```javascript
// (Optional) Executing "sql" from PATH otherwise...
"oracle-format.sqlcl": "/absolute/path/to/sql.exe",
// (Optional) Using default formatter settings otherwise...
"oracle-format.rules": "/absolute/path/to/style.xml"
// (Optional) Change languages associated with formatter
"oracle-format.languages": ["plsql" , "oraclesql"]
```

To reference a relative path inside your workspace use "${workspaceFolder}" variable:
```javascript
"oracle-format.rules": "${workspaceFolder}/.vscode/style.xml"
```

### Format on Save

If you are seeing the following warning message in the Developer Tools Console after running "formatOnSave":
```bash
WARN Aborted format on save after 750ms
```

then you need to increase the VS Code default timeout option as formatting can take quite some time for larger files:
```javascript
"editor.formatOnSaveTimeout": 10000
```

## Prerequisites

- Oracle SQLcl
- [Language PL/SQL](https://marketplace.visualstudio.com/items?itemName=xyz.plsql-language) or [Oracle Developer Tools for VS Code](https://marketplace.visualstudio.com/items?itemName=Oracle.oracledevtools)

## Note
The output from SQLcl command is printed to Output channel ("oracle-format").