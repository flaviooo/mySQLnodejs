# mySQLnodejs
## Install




cd C:\wrkNodeJS
git clone https://github.com/flaviooo/mySQLnodejs
cd mySQLnodejs
mkdir dumps
npm init -y
npm install dotenv --save 
node dump.js 
## Tool import/export DB mySQL Nodejs

* Usage: for export: node dump.js --export
* Usage: for import: node dump.js --import  -->default value DUMPFILE_IMPORT .env');
* Usage: for import: node dump.js --import dump.sql -->Path file dumps/');

### launch.json

    {
    "version": "0.2.0",
    "configurations": [

        {
            "type": "node",
            "request": "launch",
            "name": "Launch Program",
            "program": "${workspaceFolder}\\etc\\mySQLtool\\dump.js",
            "args": [
                "--import",  
              //"--import", "${workspaceFolder}\\etc\\mySQLtool\\dumps\\dump.sql"
              // "--export"
            ],
            "runtimeArgs": [
            //    "${workspaceFolder}\\etc\\mySQLtool\\dumps\\dump.sql"
            ],
            "envFile": "${workspaceFolder}\\etc\\mySQLtool\\.env"
        }
    ]
}
