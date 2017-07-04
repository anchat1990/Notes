# Notes 

## Shell Job Control	

Ctlr + Z to exit the command
> bg 
to set in background
> fg 
to set in foreground  


## Gerrit	
> git remote add --fetch --no-tags gerrit git+ssh://anweshac@gerrit.beaker-project.org:29418/beaker-in-a-box

> seahorse
 to unlock key

> ssh -vv -o IdentityAgent=none -p <port> <url>
ssh into gerrit to check whats going on. -o option is to disable ssh agent

## partitioning

### see disk names
sudo blkid 
### check space 
sudo fdisk -l /dev/nvme0n1

### resize physical partitions
sudo pvresize /dev/mapper/luks-b7ba71a1-dad5-4d2d-a841-da7f00b8eb69

### resize logical partitions
sudo lvextend /dev/fedora/root -L 100G


### resize to filesystem (partition name is the name of logical volume use
### > sudo lvs < to find name  
sudo resize2fs /dev/fedora/root

### list physical volumes
sudo pvs



## Code Reviews	

(16:57:53) dcallagh: so we use Gerrit for code reviews
(16:58:13) dcallagh: we use it for *all* the code reviews -- for beaker itself, and also for all the other separate git repos like beaker-in-a-box
(16:58:26) dcallagh: so you could post a patch to Gerrit to remove Centos 5 from beaker-in-a-box :-)
(16:59:24) dcallagh: there is some info about how to post a patch here: https://beaker-project.org/dev/guide/writing-a-patch.html
(16:59:43) dcallagh: just bear in mind -- that doc is talking about how to post a patch for beaker itself, whereas you are working on beaker-in-a-box which is separate
(16:59:51) dcallagh: so the info in that doc does not all apply directly
(17:00:38) dcallagh: step 1 would be, get yourself logged in to gerrit at https://gerrit.beaker-project.org/
(17:00:46) dcallagh: then i can give you a hand to post your patch if need be


## Beaker in a box 

virt-manager for gui 
changed is good in ansible, OK didnt have to do anything
