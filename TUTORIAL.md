# How to setup the Mario Royale server emulator

## Windows

### 1. Download the source code
You can use [Git for Windows](https://git-scm.com/download/win).
Open a command line, go to your working folder and run `git clone` followed by the clone URL given by github.

### 2. Create server config
Copy the file named `server.cfg.xml` to `server.cfg`. Feel free to change the config to your liking. However some options need to be set in later steps.

### 3. Install mysql
Get it from [https://dev.mysql.com/downloads/mysql/].
Once it is installed you can run it with the following command:

`mysqld --console`

Note which port it listens on, for example:

`Server hostname (bind-address): '*'; port: 3306`

In `server.cfg` update the `MySqlHost` (usually to localhost), `MySqlPort` (the port number above), `MySqlUser`, `MySqlPass` and `MySqlDb` (these depend on how you installed mysql) settings.

### 4. Install Python
https://www.python.org/ has the latest version. If you already have Python installed, you might need to upgrade to the latest.

### 5. Launch the server
Once mysql is running, open another console and type `python server.py`. It should start up without any errors, and start printing lines that look like:

`2020-01-28 22:56:18+0000 [-] pc: 0, mc: 0, in: 0, out: 0`

If you can see this your installation is correct.
