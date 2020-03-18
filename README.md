# aws-tooling
Various tools for Managing AWS Infrastructure


# ssm-patching
This template sets up a patch scan, based on a cron expression across three AZs, and three individual patch installation events with separate schedules.  The Patch Group is created based on a key/value (e.g. PatchGroup:Windows). The staggering of installation based on AZ requires that Availability Zone for the instance is written in a tag as well (e.g. AZ:ap-southeast-2a).  Consider using cfn-init or userdata to poll the metadata service to retrieve AZ and write it to a tag.

To deploy, run this template for each OS that is required. Copy/Paste in the type of patches required on your schedule and provide the tag key names.
