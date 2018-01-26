---
layout: layout.pug
navigationTitle:  Managing AWS
title: Managing AWS
menuWeight: 9
excerpt:

enterprise: false
---

<!-- This source repo for this topic is https://github.com/dcos/dcos-docs -->


## Scaling an AWS cluster

The DC/OS AWS CloudFormation template is optimized to run DC/OS, but you might want to change the number of agent nodes based on your needs.

**Important:** Scaling down your AWS cluster could result in data loss. It is recommended that you scale down by 1 node at a time, letting the DC/OS service recover. For example, if you are running a DC/OS service and you scale down from 10 to 5 nodes, this could result in losing all the instances of your service.

To change the number of agent nodes with AWS:

1.  From [AWS CloudFormation Management][3] home page, click on the **Services** tab on the top left-hand corner, select **CloudFormation** under the **Management Tools** header, select your DC/OS cluster and click **Update Stack**.
2.  Select **Use current template** and click next to go to the **Specify Details** section, and now you can specify new values for the **PublicSlaveInstanceCount** and **SlaveInstanceCount**.
3.  On the **Options** page, accept the defaults and click **Next**. **Tip:** You can choose whether to rollback on failure. By default this option is set to **Yes**.
4.  On the **Review** page, check the acknowledgement box and then click **Update**.

Your new machines will take a few minutes to initialize; you can watch them in the EC2 console. The DC/OS web interface will update as soon as the new nodes register.

<!-- ## Upgrading

See the upgrade [documentation](/1.11/installing/oss/cloud/aws/upgrading/). -->

 [2]: /1.11/installing/oss/cloud/aws/
 [3]: https://console.aws.amazon.com/cloudformation/home