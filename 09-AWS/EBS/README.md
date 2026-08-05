. Create EBS (Elastic Block Store) inside Volume  for EC2 

just do this step's..

. first click on button which content " Create Volume "


. Create volume Info
Create an Amazon EBS volume to attach to any EC2 instance in the same Availability Zone.

Volume settings
. Volume type
Info

. General Purpose SSD (gp3)
Size (GiB)...Info
100
Min: 1 GiB, Max: 65536 GiB.

. IOPS..Info
3000
Min: 3000 IOPS, Max: 80000 IOPS.

Throughput (MiB/s)..Info
125
Min: 125 MiB, Max: 2000 MiB. Baseline: 125 MiB/s.

. Availability Zone...Info

for ex.  eun1-az1 (eu-north-1a)   this is specific from selected region 


. Snapshot ID - it's  optional...Info

if you want to create volume from an snapshot for some another zone.. just add avialibilty zone 
for example...

Don't create volume from a snapshot > it's Default when you ensure which zone for create just add
like this 

inside box> "  snap-093ff426d8cf5bcea   "

. Encryption...Info
Use Amazon EBS encryption as an encryption solution for your EBS resources associated with your EC2 instances.
Encrypt this volume >  if you want add so just click checkbox 

. Tags - optional Info
A tag is a label that you assign to an AWS resource. Each tag consists of a key and an optional value. You can use tags to search and filter your resources or track your AWS costs.

No tags associated with the resource.
Add new tag

. final step is just click the button of which is content  " Create Volume " 

Note:- but remember if you want to more one create an volume from snapshot you must be add an tag 

