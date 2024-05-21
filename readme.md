# To use https

Create the self-signed certificate and key files:

``` bash
createcert.bat
```

This will create two file, localhost.crt and localhost.key.

now we need to register the certificate as trusted since is self-signed.

In the Certificate Manager (certmgr.msc), you can find this location by following these steps:

Open the Certificate Manager. You can do this by typing certmgr.msc into the Run dialog (Win + R).
In the Certificate Manager, expand the Certificates - Current User tree in the left pane.
Under this, expand the Trusted Root Certification Authorities folder.
Click on the Certificates folder under Trusted Root Certification Authorities. This is the equivalent location to Cert:\CurrentUser\Root in PowerShell.
then

In the Certificate Manager (certlm.msc), you can find this location by following these steps:

1. Open the Certificate Manager for Local Machine. You can do this by typing `certlm.msc` into the Run dialog (Win + R).
2. In the Certificate Manager, expand the `Certificates (Local Computer)` tree in the left pane.
3. Under this, expand the `Personal` folder.
4. Click on the `Certificates` folder under `Personal`. 

Now nginx will use the certificate and key files to serve https. And you should be fine.