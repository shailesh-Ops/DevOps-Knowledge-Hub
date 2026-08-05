
this creation are have 3 step's ...


" Specify settings
Step 2
Configure schedule 1 - Schedule 1
Step 3
Review and create "
it's step [1]

This service is provide Amazon Data Lifecycle Manager. 
Automate the creation, retention, copy and deletion of snapshots and AMIs

for create  lifecycle manager just selete those wanted... service 
you can see like this  format of 

Create new lifecycle policy
Create custom or default policy
Custom policy
Default policy

Policy type
EBS snapshot policy
EBS-backed AMI policy
Cross-account event copy policy 

Next step  

select you're  creation point  and  Policy type after just click the  " Next step "

after...click 

I'm show you custom Policy and policy type EBS snapshot policy this step ensure all point..

Specify settings
>>Target resources Info....
Specify the resources that are to be targeted by this policy.

Target resource types
Select the type of resources that are to be targeted.
Volume
Instance


>>Target resource tags
All resources of the selected type that have at least one of these tags will be targeted by the policy.
Add
45 tags remaining of 45.


>>Description
Policy description
IAM role Info
This policy must be associated with an IAM role that has the appropriate permissions. If you choose to create a new role, you must grant relevant role permissions and set up trust relationships correctly. If you are unsure of what role to use, choose Default role.

Default role
If the default role already exists, Amazon Data Lifecycle Manager will use that role. If it does not exist yet, it will be automatically created with all the required permissions.

>>View default role permissions
for ex.. {
	"Version": "2012-10-17",
	"Statement": [
		{
			"Effect": "Allow",
			"Action": [
				"ec2:CreateSnapshot",
				"ec2:CreateSnapshots",
				"ec2:DeleteSnapshot",
				"ec2:DescribeInstances",
				"ec2:DescribeVolumes",
				"ec2:DescribeSnapshots",
				"ec2:EnableFastSnapshotRestores",
				"ec2:DescribeFastSnapshotRestores",
				"ec2:DisableFastSnapshotRestores",
				"ec2:CopySnapshot",
				"ec2:ModifySnapshotAttribute",
				"ec2:DescribeSnapshotAttribute",
				"ec2:DescribeSnapshotTierStatus",
				"ec2:ModifySnapshotTier"
			],
			"Resource": "*"
		},
		{
			"Effect": "Allow",
			"Action": [
				"ec2:CreateTags"
			],
			"Resource": "arn:aws:ec2:*::snapshot/*"
		},
		{
			"Effect": "Allow",
			"Action": [
				"ec2:CreateTags",
				"events:PutRule",
				"events:DeleteRule",
				"events:DescribeRule",
				"events:EnableRule",
				"events:DisableRule",
				"events:ListTargetsByRule",
				"events:PutTargets",
				"events:RemoveTargets"
			],
			"Resource": "arn:aws:events:*:*:rule/AwsDataLifecycleRule.managed-cwe.*"
		}
	]
}

if you want..
>>Choose another role  ... just click small Box 
AWSDataLifecycleManagerDefaultRole
AWSServiceRoleForResourceExplorer
AWSServiceRoleForSupport
AWSServiceRoleForTrustedAdvisor

        Or SELECT 

>> Create a new IAM role 

>>Tags - optional Info
Assign custom tags to the policy to help you identify, organize, and secure your lifecycle policies. Each tag consists of a key and an optional value.

No tags associated with the resource.
Add new tag
You can add up to 50 tags.

>>Policy status
Specify whether to enable the policy immediately after creation or modification. If you do not enable the policy now, then it will not begin creating snapshots or AMIs until you manually set its activation status to enabled.

Enabled
Not enabled

it's step [2]

>>Configure schedule 1 - Schedule 1
Schedules define how often the policy runs and the specific actions that are to be performed. The policy must have at least one schedule.

Additional schedules must have the same retention type as Schedule 1, but they can have their own retention count or age. Snapshot archiving can be enabled for one schedule only.

>>Schedule details Info

You can add 3 more schedules to this policy.
Schedule name
Schedule 1
Frequency

Daily
Every

12 hours
Starting at
09:00
UTC
Retention type

Count Keep  snapshots in standard tier

and final step is Review policy  

it's step [3]

then click  the button   "  Review policy  "
