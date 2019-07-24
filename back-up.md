# Back Up

## Linux backup

```shell
# Using following rsync options
#   v  Verbose
#   u  Update. Only update the target if source is newer
#   r  Recursive. 

rsync -vur /home/nzhang/storage/ ./ned_ibm/storage | tee -a ./ned_ibm/storage/linux_backup.log
```

## Windows backup

```cmd

SET BACK_DST=d:\backup\ned_ibm\storage
SET BACK_OPT=/E /COPY:DAT /XO /LOG+:%BACK_DST%\win_backup.log /NP /TEE

robocopy t:\installer %BACK_DST%\installer %BACK_OPT%
robocopy t:\knowledge %BACK_DST%\knowledge %BACK_OPT%
robocopy t:\project %BACK_DST%\project %BACK_OPT%

```
