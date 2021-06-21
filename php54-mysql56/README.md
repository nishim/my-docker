# PHP5.4 + MySQL5.6

## DB接続
```
mysql -u user -p -h 127.0.0.1 -P 33306 -D db
```

## VSCodeでのデバッグ

.vscode/launch.json
```
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Listen for XDebug",
            "type": "php",
            "request": "launch",
            "port": 9000,
            "pathMappings": {
                "/var/www/html":"${workspaceRoot}"
            }
        }
    ]
}
```