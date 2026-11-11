# tOOl

## evaluate_submission_process.sh

Usage: evaluate_submission_process.sh $prj $pkg
Valid $prj: SLE-15, SLE-15-SP1 ... SLE-15-SP7, SLE-16.0, SLE-16.1

Example:
$ evaluate_submission_process.sh SLE-15-SP3 gdm
GNOME:STABLE:3.34
 -> SUSE:SLE-15-SP2:Update # It means SP3/gdm inherits from SP2:Update/gdm, so submitting to SP2:Update is sufficient to benifit both

$ evaluate_submission_process.sh SLE-15-SP1 flatpak
Devel:Desktop:SLE-15-SP1 # It means flatpak has a fork in SP1 hosted in Devel:Desktop
 -> SUSE:SLE-15-SP1:Update
