# tOOl

## evaluate_submission_process.sh

__Usage__

evaluate_submission_process.sh *$prj [SLE-15, SLE-15-SP1 ... SLE-15-SP7, SLE-16.0, SLE-16.1] $pkg [Package_Name]*

__Examples__

> What the following command tells the order to submit SUSE:SLE-15-SP3:Update/gdm:
> 
> Submit first to GNOME:STABLE:3.34 as the developement project
> 
> Submit then to SUSE:SLE-15-SP2:Update. Implicitly it means SP3/gdm inherits from SP2:Update/gdm, so submitting to SP2:Update is sufficient to benifit both.

$ evaluate_submission_process.sh SLE-15-SP3 gdm

GNOME:STABLE:3.34 

 -> SUSE:SLE-15-SP2:Update 

> Likewise, the command below tells the order to sumit SUSE:SLE-15-SP1:Update/flatpak:
> 
> Submit first to Devel:Desktop:SLE-15-SP1 as the development project (forked from SLE-15)
> 
> Submit then to SUSE:SLE-15-SP1:Update

$ evaluate_submission_process.sh SLE-15-SP1 flatpak

Devel:Desktop:SLE-15-SP1
 
 -> SUSE:SLE-15-SP1:Update

> This is an example when there is a **difference between the devel and
> maintenance project**. Usually it means, before your real work,
> reviewing the difference and do the necessary sync is highly
> recommented. Otherwise, you will probably need to rebase your work
> any way.
>
> Please notice the difference may have very various meanings.
>
> For example, if a previously submission has not been accepted by
> maintenance will cause the package in the devel project ahead that in
> the maintenance project.
>
> On the other hand, if a previous sumission did not go through the
> development project while accepted by the maintenance project, the
> package in the maintenance project will be ahead that in the devel
> project.
>
> There might be more complicated issue that a package has a big
> incremental divergence between devel project and maintenance
> project.
> 
> Thus, usually the difference will need a **manual review** to decide
> what to do. As a general recommendation, **synchronizing the package
> or clarifying the difference before a real work** are highly
> recommended.


$ evaluate_submission_process.sh SLE-15-SP4 gdm

GNOME:STABLE:41

 -> SUSE:SLE-15-SP4:Update

Warning: Differences detected for package gdm between GNOME:STABLE:41 and SUSE:SLE-15-SP4:Update.

Do you want to review the differences? (y/N): y
