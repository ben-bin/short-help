# Install PHP for Windows
[Manuals Windows](index.md)

For more information check site [PHP for Windows](https://windows.php.net)

### Step 1: Download the PHP files
Get the latest PHP x64 ZIP package from [Site](https://windows.php.net/download/)

### Step 2: Extract the files
Create a new `php` folder in the root of your `C:\ ` drive and extract the
content of the ZIP into it.

>You can install PHP anywhere on your system, but you’ll need to change the
> paths referenced below if you use anything other than `C:\php`.

### Step 3: Configure `php.ini`
PHP’s configuration file is `php.ini`. This doesn’t exist initially, so copy
`C:\php\php.ini-development` to `C:\php\php.ini`. This default configuration
provides a development setup which reports all PHP errors and warnings.

You can edit `php.ini` in a text editor, and you may need to change lines such
as those suggested below (use search to find the setting). In most cases,
you’ll need to remove a leading semicolon (;) to uncomment a value.

First, enable any required extensions according to the libraries you want to use.
The following extensions should be suitable for most applications including.

### Step 4: Add `C:\php` to the `PATH` environment variable
To ensure Windows can find the PHP executable, you must add it to the `Path` 
environment variable. Click the __Windows Start__ button and type “environment”,
then click __Edit the system environment variables__. Select the __Advanced__
tab, and click the __Environment Variables__ button.

Scroll down the __System variables__ list and click __Path__, followed by the
__Edit__ button. Click __New__ and add `C:\php`.

Or use CMD run as Administrator and make command
```cmd
setx Path "%Path%C:\php;" /M
```

If you have extracted PHP to a different folder, such as `C:\other\folder`, you
will need to execute the following command use CMD as Administrator:
```cmd
mklink /D C:\php C:\other\folder
```