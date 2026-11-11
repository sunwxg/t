# tOOl

## evaluate_submission_process.sh

__Usage__

evaluate_submission_process.sh *$prj [SLE-15, SLE-15-SP1 ... SLE-15-SP7, SLE-16.0, SLE-16.1] $pkg [Package_Name]*

__Examples__

> What the following command tells the order to submit SUSE:SLE-15-SP3:Update/gdm:
> Submit first to GNOME:STABLE:3.34 as the developement project
> Submit then to SUSE:SLE-15-SP2:Update. Implicitly it means SP3/gdm inherits from SP2:Update/gdm, so submitting to SP2:Update is sufficient to benifit both.

$ evaluate_submission_process.sh SLE-15-SP3 gdm

GNOME:STABLE:3.34 

 -> SUSE:SLE-15-SP2:Update 
 

> Likewise, the command below tells the order to sumit SUSE:SLE-15-SP1:Update/flatpak:
> Submit first to Devel:Desktop:SLE-15-SP1 as the development project (forked from SLE-15)
> Submit then to SUSE:SLE-15-SP1:Update

$ evaluate_submission_process.sh SLE-15-SP1 flatpak

Devel:Desktop:SLE-15-SP1
 
 -> SUSE:SLE-15-SP1:Update
