Fiscal Officer Cannot Edit Accounting Lines or Approve POA
======================

This git repository represents the University of Arizona (the UA)'s _Fiscal Officer Cannot Edit Accounting Lines or Approve POA_ modification to **KFS 3.0**, in the form of patch files (generated by svn diff), liquibase scripts, and documentation.
This "patch package" is designed to be informative to technical developers in the position to
apply patch files to the java source code of KFS. In order to better serve such an endeavor,
this README contains several informative sections:

* <a href="#jiras">List of Jiras</a> - This list contains every Jira ticket at the University of Arizona
  that relates to this modification. It provides reverse documentation back to the developers at
  the UA in case of questions regarding how this patch package was created.
* <a href="#liquibase-changesets">List of Liquibase Changesets</a> - This list contains any
  liquibase changeset files that were associated with this modification.
* <a href="#patch-files">List of Patch Files</a> - This is a list of each patch file that needs
  to be applied to the KFS source code in order to realize the modification. This list does _not_
  include patch files for revisions that didn't touch the `trunk/` at the UA.
  Before a modification was merged with `trunk/`, it may have been tweaked, reworked, refactored,
  code reviewed, etc, in handfuls of revisions in a feature branch.
* <a href="#revisions">List of Revisions</a> - This list contains every revision associated with
  this modification. Many of which, as you will see, only touch files in a feature branch. The
  revisions that actually made it into the actual modification touch files in `trunk/`. The list
  of patch files is a better reference of which are these revisions.
* <a href="#files">Lists of Files</a> - These lists contain every file that was created,
  modified, or deleted for this enhancement.
* <a href="#post-mod-changes">List of Post-Modification Changes</a> - This list contains
  revision numbers that are _not_ included in the patches, or raw patches, but that touched one
  or more key files involved in this modification.

<h2>Jiras</h2>

This is a list of Jira tickets at the University of Arizona that relate to this modification. The subversion revisions tagged against each such jira are also listed:

* **KFSI-4978**: (Fiscal Officer Cannot Edit Accounting Lines or Approve POA)<br />
  revisions: #21244, #21423

<h2>Liquibase Changesets</h2>

There are no liquibase changesets associated with this modification.

<h2>Patch Files</h2>

This is a list of all of the patches for revisions that affected files in `trunk/`. The filenames in each has been modified, for easy digestion. UA's subversion server manages many Kuali projects in one Subversion project, so a file path like:

```
financial-system/kfs/trunk/src/org/kuali/kfs...
```

has been modified to:

```
src/org/kuali/kfs...
```

* [`patches/21244_KFSI-4978_cleaned.diff`](Fiscal-Officer-Cannot-Edit-Accounting-Lines-or-Approve-POA/blob/master/patches/21244_KFSI-4978_cleaned.diff) is the patch file for #21244.
* [`patches/21423_KFSI-4978_cleaned.diff`](Fiscal-Officer-Cannot-Edit-Accounting-Lines-or-Approve-POA/blob/master/patches/21423_KFSI-4978_cleaned.diff) is the patch file for #21423.

<h2>Revisions</h2>

This is an ordered list of revisions that relate to this modification. There may not be a patch
file for every revision listed below for the following reasons:

* A revision might only affect a branch, perhaps one where development primarily took place. Any
  changes that finally made it into `trunk/` will be seen in revisions that specifically touch
  files in `trunk/`. Therefore, we do not create patch files for revisions that only affect a
  branch.
* A revision might only include a liquibase changeset that is executed by some automated process.
  Since each institution maintains different revision controls on their database, liquibase
  changesets are not provided as patches. They are instead presented as intact files under the
  `liquibase-changesets/` directory.

[Here](Fiscal-Officer-Cannot-Edit-Accounting-Lines-or-Approve-POA/blob/master/patch_log.txt) is a printout of `svn log -v` for each revision.

*   \#21244 was committed against KFSI-4978 on 2011-08-18 19:24:47 UTC by <strong>kevinmco@CATNET.ARIZONA.EDU</strong>.

    > KFSI-4978 KITT-2848 Fiscal Officer can not edit Accounting Lines
*   \#21423 was committed against KFSI-4978 on 2011-08-29 23:52:05 UTC by <strong>jpbriede@CATNET.ARIZONA.EDU</strong>.

    > KFSI-4978
    > KITT-2848
    > Updating the accounting lines on a PurchaseOrderAmendmentDocument before saving so the accounting line amounts reflect any change in the accounting line percentages.

<h2>Files</h2>

Files **modified** for this modification (4 files)

    /work/src/edu/arizona/kfs/module/purap/PurapWorkflowConstants.java
    /work/src/edu/arizona/kfs/module/purap/document/authorization/UaPurchaseOrderAmendmentDocumentPresentationController.java
    /work/src/org/kuali/kfs/module/purap/document/PurchaseOrderAmendmentDocument.java
    /work/src/org/kuali/kfs/module/purap/document/authorization/PurchaseOrderAmendmentDocumentPresentationController.java

<h2>Extra Local Files</h2>

Extra local files for this modification that have been included for some reason or another. Most likely, these files are not code, but instead might be specifications, or other documentation. (2 files)

* [`extra_files/KFSI-4978.odg`](Fiscal-Officer-Cannot-Edit-Accounting-Lines-or-Approve-POA/blob/master/extra_files/KFSI-4978.odg)
* [`extra_files/KFSI-4978.txt`](Fiscal-Officer-Cannot-Edit-Accounting-Lines-or-Approve-POA/blob/master/extra_files/KFSI-4978.txt)

<h2>Post Mod Changes</h2>

For each file that was changed or added for this modification, I've looked at its history in subversion (`svn log <file_name>`) to find whether later fixes were committed against this modification that I might have missed. There were some :) They may be fixes to the modification, or further enhancements, or changes completely unrelated. Please contact the UA for more information about a given revision number, or Jira ticket. Here they are:

*   **#23309** touches /work/src/org/kuali/kfs/module/purap/document/PurchaseOrderAmendmentDocument.java.

    > KFSI-5448
*   **#23611** touches /work/src/org/kuali/kfs/module/purap/document/PurchaseOrderAmendmentDocument.java.

    > KFSI-5448
*   **#24306** touches /work/src/edu/arizona/kfs/module/purap/PurapWorkflowConstants.java.

    > KFSI-6365/KATTS-39/KITT-3076 PREQ documents from eInvoice routing to kfs-sys-user as initiator of PREQ

(3 revisions)

