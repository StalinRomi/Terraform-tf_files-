## Taint command is used to tell terraform that a object is degraded / damaged.

Terraform then marks this resource as tainted in statefile & next time, it will tell you need to replace it.

## State Rollback -

We can rollback to the previous version of the statefile.

If we using S3 for terraform state, we can use AWS api / cli to versions of S3 -> Take copy of pervious version -> Copy in to local -> Push local copy to remote

Now the pervious version becomes the new version.

### Its not recommended, since we can create next stage.
