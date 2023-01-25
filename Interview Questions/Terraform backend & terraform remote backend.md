## Wherever, statefile is stored -> Terraform backend

Statefile Keeps a track of resources that Terraform is managing

## Remote backend is used when we are using terraform with a team / collaborating with others

If you're storing terraform statefile in your computer, then there's a chance that multiple people can try to access script at a time & **conflicting requests happen**.

Eg. One person trying to create ec2 instance, while other one trying to delete it.

### We can keep terraform statefile in S3 bucket and enable locking with it.

When one person is trying to access this terraform statefile, no other person should be allowed & they can be notfied that someone is using it at this moment.
