# Creating New AMI

## If there is sufficient space
1. Install everything necessary.
2. Take snapshot.
3. Build image from snapshot.
4. Change ec2.py script to load this image upon "ni-launch" command

## If we need to expand the disk
(Do this all before everything above)
1. Detach root volume
2. Take snapshot of volume
3. Build new larger volume with snapshot
4. [Expand partition](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/storage_expand_partition.html)
5. [Extend Filesystem](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-expand-volume.html#recognize-expanded-volume-linux)
6. Reattach volume as boot device.
7. Follow above steps