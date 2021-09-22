## Initial Users

## Set up databasae
* database first to create Globomantics database
* InitializeGlobomanticsDb.sql
* code first to create GlobomanticsIdSrv database
* DbContext for the IdentityServer operational data.
* update-database -migration 20201103152410_InitialMigration -context ConfigurationDbContext
* DbContext for the IdentityServer configuration data.
* update-database -migration 20201103152457_InitialMigration -context PersistedGrantDbContext

The database creation logic above will create the following users: Run InitializeGlobomanticsDb.sql
* rr@acme.com / `l00neyTunes!`
* wile@acme.com / `l00neyTunes!`
* kim@mars.com / `to1nfinity!`
* stanley@mars.com / `to1nfinity!`

## Setup Notes (Old Way)
* [SQL Server Express](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
* [Papercut](https://github.com/ChangemakerStudios/Papercut-SMTP) -- This is Windows-only and is replaced in our Docker setup

## Preparing Your Workstation for Containers
* [Docker Desktop](https://www.docker.com/products/docker-desktop)
* [Install and Configure Windows Terminal](https://gist.github.com/dahlsailrunner/ec99e195b2a4903748a74df64a1f1a94)
* [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

## Download smtp4deve and run it in dock
* Download it from windows terminal > docker pull ruwood/smtp4dev
* Run it and check
![image](https://user-images.githubusercontent.com/64368109/134342917-7237e15a-5bcd-407d-8649-d75bcc7a80bc.png)


## SSL With Docker Compose and nginx as Reverse Proxy
https://gist.github.com/dahlsailrunner/679e6dec5fd769f30bce90447ae80081

## Local Kubernetes Setup
Just use the Docker Desktop Kubernetes instance (enable it in Settings within Docker Desktop).

Then here are some handy notes: 
https://gist.github.com/dahlsailrunner/1a47b0e38f6e3ba64d4d61835c73b7e2

## Excluding Health Checks from Serilog Request Logging
Great blog post by Andrew Lock on this very topic:
https://andrewlock.net/using-serilog-aspnetcore-in-asp-net-core-3-excluding-health-check-endpoints-from-serilog-request-logging/
