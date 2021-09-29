# API Reference <a name="API Reference"></a>

## Constructs <a name="Constructs"></a>

### FargateJobExecutor <a name="cdk-gitlab.FargateJobExecutor"></a>

The FargateJobExecutor.

#### Initializers <a name="cdk-gitlab.FargateJobExecutor.Initializer"></a>

```typescript
import { FargateJobExecutor } from 'cdk-gitlab'

new FargateJobExecutor(scope: Construct, id: string, props?: FargateJobExecutorProps)
```

##### `scope`<sup>Required</sup> <a name="cdk-gitlab.FargateJobExecutor.parameter.scope"></a>

- *Type:* [`@aws-cdk/core.Construct`](#@aws-cdk/core.Construct)

---

##### `id`<sup>Required</sup> <a name="cdk-gitlab.FargateJobExecutor.parameter.id"></a>

- *Type:* `string`

---

##### `props`<sup>Optional</sup> <a name="cdk-gitlab.FargateJobExecutor.parameter.props"></a>

- *Type:* [`cdk-gitlab.FargateJobExecutorProps`](#cdk-gitlab.FargateJobExecutorProps)

---



#### Properties <a name="Properties"></a>

##### `region`<sup>Required</sup> <a name="cdk-gitlab.FargateJobExecutor.property.region"></a>

```typescript
public readonly region: string;
```

- *Type:* `string`

---

##### `taskDefinitionArn`<sup>Required</sup> <a name="cdk-gitlab.FargateJobExecutor.property.taskDefinitionArn"></a>

```typescript
public readonly taskDefinitionArn: string;
```

- *Type:* `string`

task definition arn.

---

##### `cluster`<sup>Optional</sup> <a name="cdk-gitlab.FargateJobExecutor.property.cluster"></a>

```typescript
public readonly cluster: ICluster;
```

- *Type:* [`@aws-cdk/aws-ecs.ICluster`](#@aws-cdk/aws-ecs.ICluster)

---

##### `securityGroup`<sup>Optional</sup> <a name="cdk-gitlab.FargateJobExecutor.property.securityGroup"></a>

```typescript
public readonly securityGroup: ISecurityGroup;
```

- *Type:* [`@aws-cdk/aws-ec2.ISecurityGroup`](#@aws-cdk/aws-ec2.ISecurityGroup)

---

##### `subnet`<sup>Optional</sup> <a name="cdk-gitlab.FargateJobExecutor.property.subnet"></a>

```typescript
public readonly subnet: ISubnet;
```

- *Type:* [`@aws-cdk/aws-ec2.ISubnet`](#@aws-cdk/aws-ec2.ISubnet)

---


### FargateRunner <a name="cdk-gitlab.FargateRunner"></a>

The FargateRunner.

#### Initializers <a name="cdk-gitlab.FargateRunner.Initializer"></a>

```typescript
import { FargateRunner } from 'cdk-gitlab'

new FargateRunner(scope: Construct, id: string, props: FargateRunnerProps)
```

##### `scope`<sup>Required</sup> <a name="cdk-gitlab.FargateRunner.parameter.scope"></a>

- *Type:* [`@aws-cdk/core.Construct`](#@aws-cdk/core.Construct)

---

##### `id`<sup>Required</sup> <a name="cdk-gitlab.FargateRunner.parameter.id"></a>

- *Type:* `string`

---

##### `props`<sup>Required</sup> <a name="cdk-gitlab.FargateRunner.parameter.props"></a>

- *Type:* [`cdk-gitlab.FargateRunnerProps`](#cdk-gitlab.FargateRunnerProps)

---



#### Properties <a name="Properties"></a>

##### `vpc`<sup>Required</sup> <a name="cdk-gitlab.FargateRunner.property.vpc"></a>

```typescript
public readonly vpc: IVpc;
```

- *Type:* [`@aws-cdk/aws-ec2.IVpc`](#@aws-cdk/aws-ec2.IVpc)

---


### Provider <a name="cdk-gitlab.Provider"></a>

The Provider to create GitLab Integrations with AWS.

#### Initializers <a name="cdk-gitlab.Provider.Initializer"></a>

```typescript
import { Provider } from 'cdk-gitlab'

new Provider(scope: Construct, id: string, props?: ProviderProps)
```

##### `scope`<sup>Required</sup> <a name="cdk-gitlab.Provider.parameter.scope"></a>

- *Type:* [`@aws-cdk/core.Construct`](#@aws-cdk/core.Construct)

---

##### `id`<sup>Required</sup> <a name="cdk-gitlab.Provider.parameter.id"></a>

- *Type:* `string`

---

##### `props`<sup>Optional</sup> <a name="cdk-gitlab.Provider.parameter.props"></a>

- *Type:* [`cdk-gitlab.ProviderProps`](#cdk-gitlab.ProviderProps)

---

#### Methods <a name="Methods"></a>

##### `createEksCluster` <a name="cdk-gitlab.Provider.createEksCluster"></a>

```typescript
public createEksCluster(scope: Construct, id: string, props: EksClusterOptions)
```

###### `scope`<sup>Required</sup> <a name="cdk-gitlab.Provider.parameter.scope"></a>

- *Type:* [`@aws-cdk/core.Construct`](#@aws-cdk/core.Construct)

---

###### `id`<sup>Required</sup> <a name="cdk-gitlab.Provider.parameter.id"></a>

- *Type:* `string`

---

###### `props`<sup>Required</sup> <a name="cdk-gitlab.Provider.parameter.props"></a>

- *Type:* [`cdk-gitlab.EksClusterOptions`](#cdk-gitlab.EksClusterOptions)

---

##### `createEksServiceRole` <a name="cdk-gitlab.Provider.createEksServiceRole"></a>

```typescript
public createEksServiceRole()
```

##### `createFargateEksCluster` <a name="cdk-gitlab.Provider.createFargateEksCluster"></a>

```typescript
public createFargateEksCluster(scope: Construct, id: string, props: FargateEksClusterOptions)
```

###### `scope`<sup>Required</sup> <a name="cdk-gitlab.Provider.parameter.scope"></a>

- *Type:* [`@aws-cdk/core.Construct`](#@aws-cdk/core.Construct)

---

###### `id`<sup>Required</sup> <a name="cdk-gitlab.Provider.parameter.id"></a>

- *Type:* `string`

---

###### `props`<sup>Required</sup> <a name="cdk-gitlab.Provider.parameter.props"></a>

- *Type:* [`cdk-gitlab.FargateEksClusterOptions`](#cdk-gitlab.FargateEksClusterOptions)

---

##### `createFargateRunner` <a name="cdk-gitlab.Provider.createFargateRunner"></a>

```typescript
public createFargateRunner(executor?: FargateJobExecutor)
```

###### `executor`<sup>Optional</sup> <a name="cdk-gitlab.Provider.parameter.executor"></a>

- *Type:* [`cdk-gitlab.FargateJobExecutor`](#cdk-gitlab.FargateJobExecutor)

---

##### `createGitlabManagedEksRole` <a name="cdk-gitlab.Provider.createGitlabManagedEksRole"></a>

```typescript
public createGitlabManagedEksRole(props: RoleProps)
```

###### `props`<sup>Required</sup> <a name="cdk-gitlab.Provider.parameter.props"></a>

- *Type:* [`cdk-gitlab.RoleProps`](#cdk-gitlab.RoleProps)

---

##### `createSecurityGroup` <a name="cdk-gitlab.Provider.createSecurityGroup"></a>

```typescript
public createSecurityGroup()
```


#### Properties <a name="Properties"></a>

##### `vpc`<sup>Required</sup> <a name="cdk-gitlab.Provider.property.vpc"></a>

```typescript
public readonly vpc: IVpc;
```

- *Type:* [`@aws-cdk/aws-ec2.IVpc`](#@aws-cdk/aws-ec2.IVpc)

---

##### `gitlabEksRole`<sup>Optional</sup> <a name="cdk-gitlab.Provider.property.gitlabEksRole"></a>

```typescript
public readonly gitlabEksRole: IRole;
```

- *Type:* [`@aws-cdk/aws-iam.IRole`](#@aws-cdk/aws-iam.IRole)

---


## Structs <a name="Structs"></a>

### CapacityProviderStrategyItem <a name="cdk-gitlab.CapacityProviderStrategyItem"></a>

The Capacity Provider strategy.

#### Initializer <a name="[object Object].Initializer"></a>

```typescript
import { CapacityProviderStrategyItem } from 'cdk-gitlab'

const capacityProviderStrategyItem: CapacityProviderStrategyItem = { ... }
```

##### `capacityProvider`<sup>Required</sup> <a name="cdk-gitlab.CapacityProviderStrategyItem.property.capacityProvider"></a>

```typescript
public readonly capacityProvider: FargateCapacityProviderType;
```

- *Type:* [`cdk-gitlab.FargateCapacityProviderType`](#cdk-gitlab.FargateCapacityProviderType)

---

##### `weight`<sup>Required</sup> <a name="cdk-gitlab.CapacityProviderStrategyItem.property.weight"></a>

```typescript
public readonly weight: number;
```

- *Type:* `number`

---

##### `base`<sup>Optional</sup> <a name="cdk-gitlab.CapacityProviderStrategyItem.property.base"></a>

```typescript
public readonly base: number;
```

- *Type:* `number`

---

### EksClusterOptions <a name="cdk-gitlab.EksClusterOptions"></a>

#### Initializer <a name="[object Object].Initializer"></a>

```typescript
import { EksClusterOptions } from 'cdk-gitlab'

const eksClusterOptions: EksClusterOptions = { ... }
```

##### `clusterOptions`<sup>Required</sup> <a name="cdk-gitlab.EksClusterOptions.property.clusterOptions"></a>

```typescript
public readonly clusterOptions: ClusterProps;
```

- *Type:* [`@aws-cdk/aws-eks.ClusterProps`](#@aws-cdk/aws-eks.ClusterProps)

cluster properties for Amazon EKS cluster.

---

##### `rbac`<sup>Optional</sup> <a name="cdk-gitlab.EksClusterOptions.property.rbac"></a>

```typescript
public readonly rbac: boolean;
```

- *Type:* `boolean`
- *Default:* true

create serivce account and rbac ClusterRoleBinding for gitlab.

> https://docs.gitlab.com/ee/user/project/clusters/add_remove_clusters.html#add-existing-cluster

---

### FargateEksClusterOptions <a name="cdk-gitlab.FargateEksClusterOptions"></a>

#### Initializer <a name="[object Object].Initializer"></a>

```typescript
import { FargateEksClusterOptions } from 'cdk-gitlab'

const fargateEksClusterOptions: FargateEksClusterOptions = { ... }
```

##### `clusterOptions`<sup>Required</sup> <a name="cdk-gitlab.FargateEksClusterOptions.property.clusterOptions"></a>

```typescript
public readonly clusterOptions: FargateClusterProps;
```

- *Type:* [`@aws-cdk/aws-eks.FargateClusterProps`](#@aws-cdk/aws-eks.FargateClusterProps)

cluster properties for Amazon EKS cluster.

---

##### `helmRunnerOptions`<sup>Optional</sup> <a name="cdk-gitlab.FargateEksClusterOptions.property.helmRunnerOptions"></a>

```typescript
public readonly helmRunnerOptions: HelmRunnerOptions;
```

- *Type:* [`cdk-gitlab.HelmRunnerOptions`](#cdk-gitlab.HelmRunnerOptions)

Gitlab helm Chart runner install Options.

see https://docs.gitlab.com/runner/install/kubernetes.html

---

##### `rbac`<sup>Optional</sup> <a name="cdk-gitlab.FargateEksClusterOptions.property.rbac"></a>

```typescript
public readonly rbac: boolean;
```

- *Type:* `boolean`
- *Default:* true

create serivce account and rbac ClusterRoleBinding for gitlab.

> https://docs.gitlab.com/ee/user/project/clusters/add_remove_clusters.html#add-existing-cluster

---

### FargateJobExecutorProps <a name="cdk-gitlab.FargateJobExecutorProps"></a>

The properties for the FargateJobExecutor.

#### Initializer <a name="[object Object].Initializer"></a>

```typescript
import { FargateJobExecutorProps } from 'cdk-gitlab'

const fargateJobExecutorProps: FargateJobExecutorProps = { ... }
```

##### `cluster`<sup>Optional</sup> <a name="cdk-gitlab.FargateJobExecutorProps.property.cluster"></a>

```typescript
public readonly cluster: ICluster;
```

- *Type:* [`@aws-cdk/aws-ecs.ICluster`](#@aws-cdk/aws-ecs.ICluster)

---

##### `image`<sup>Optional</sup> <a name="cdk-gitlab.FargateJobExecutorProps.property.image"></a>

```typescript
public readonly image: JobExecutorImage;
```

- *Type:* [`cdk-gitlab.JobExecutorImage`](#cdk-gitlab.JobExecutorImage)

The docker image for the job executor container.

---

##### `region`<sup>Optional</sup> <a name="cdk-gitlab.FargateJobExecutorProps.property.region"></a>

```typescript
public readonly region: string;
```

- *Type:* `string`

AWS region for the job executor.

---

##### `securityGroup`<sup>Optional</sup> <a name="cdk-gitlab.FargateJobExecutorProps.property.securityGroup"></a>

```typescript
public readonly securityGroup: ISecurityGroup;
```

- *Type:* [`@aws-cdk/aws-ec2.ISecurityGroup`](#@aws-cdk/aws-ec2.ISecurityGroup)

---

##### `subnet`<sup>Optional</sup> <a name="cdk-gitlab.FargateJobExecutorProps.property.subnet"></a>

```typescript
public readonly subnet: ISubnet;
```

- *Type:* [`@aws-cdk/aws-ec2.ISubnet`](#@aws-cdk/aws-ec2.ISubnet)

---

### FargateRunnerProps <a name="cdk-gitlab.FargateRunnerProps"></a>

Properties for the FargateRunner.

#### Initializer <a name="[object Object].Initializer"></a>

```typescript
import { FargateRunnerProps } from 'cdk-gitlab'

const fargateRunnerProps: FargateRunnerProps = { ... }
```

##### `vpc`<sup>Required</sup> <a name="cdk-gitlab.FargateRunnerProps.property.vpc"></a>

```typescript
public readonly vpc: IVpc;
```

- *Type:* [`@aws-cdk/aws-ec2.IVpc`](#@aws-cdk/aws-ec2.IVpc)

VPC for the fargate.

---

##### `clusterDefaultCapacityProviderStrategy`<sup>Optional</sup> <a name="cdk-gitlab.FargateRunnerProps.property.clusterDefaultCapacityProviderStrategy"></a>

```typescript
public readonly clusterDefaultCapacityProviderStrategy: CapacityProviderStrategyItem[];
```

- *Type:* [`cdk-gitlab.CapacityProviderStrategyItem`](#cdk-gitlab.CapacityProviderStrategyItem)[]
- *Default:* DEFAULT_CLUSTER_CAPACITY_PROVIDER_STRATEGY

Default capacity provider strategy for the Amazon ECS cluster.

---

##### `executor`<sup>Optional</sup> <a name="cdk-gitlab.FargateRunnerProps.property.executor"></a>

```typescript
public readonly executor: FargateJobExecutor;
```

- *Type:* [`cdk-gitlab.FargateJobExecutor`](#cdk-gitlab.FargateJobExecutor)

Fargate job executor options.

---

##### `fargateJobSubnet`<sup>Optional</sup> <a name="cdk-gitlab.FargateRunnerProps.property.fargateJobSubnet"></a>

```typescript
public readonly fargateJobSubnet: SubnetSelection;
```

- *Type:* [`@aws-cdk/aws-ec2.SubnetSelection`](#@aws-cdk/aws-ec2.SubnetSelection)

subnet for fargate CI task.

---

##### `gitlabURL`<sup>Optional</sup> <a name="cdk-gitlab.FargateRunnerProps.property.gitlabURL"></a>

```typescript
public readonly gitlabURL: string;
```

- *Type:* `string`
- *Default:* 'https://gitlab.com'

gitlab URL prefix.

---

##### `registrationToken`<sup>Optional</sup> <a name="cdk-gitlab.FargateRunnerProps.property.registrationToken"></a>

```typescript
public readonly registrationToken: string;
```

- *Type:* `string`

GitLab registration token for the runner.

---

##### `securityGroup`<sup>Optional</sup> <a name="cdk-gitlab.FargateRunnerProps.property.securityGroup"></a>

```typescript
public readonly securityGroup: ISecurityGroup;
```

- *Type:* [`@aws-cdk/aws-ec2.ISecurityGroup`](#@aws-cdk/aws-ec2.ISecurityGroup)

The security group for Fargate CI task.

---

##### `serviceDefaultCapacityProviderStrategy`<sup>Optional</sup> <a name="cdk-gitlab.FargateRunnerProps.property.serviceDefaultCapacityProviderStrategy"></a>

```typescript
public readonly serviceDefaultCapacityProviderStrategy: CapacityProviderStrategyItem[];
```

- *Type:* [`cdk-gitlab.CapacityProviderStrategyItem`](#cdk-gitlab.CapacityProviderStrategyItem)[]
- *Default:* DEFAULT_SERVICE_CAPACITY_PROVIDER_STRATEGY

Default capacity provider strategy for the Amazon ECS service.

---

##### `tags`<sup>Optional</sup> <a name="cdk-gitlab.FargateRunnerProps.property.tags"></a>

```typescript
public readonly tags: string[];
```

- *Type:* `string`[]

tags for the runner.

---

### HelmRunnerOptions <a name="cdk-gitlab.HelmRunnerOptions"></a>

#### Initializer <a name="[object Object].Initializer"></a>

```typescript
import { HelmRunnerOptions } from 'cdk-gitlab'

const helmRunnerOptions: HelmRunnerOptions = { ... }
```

##### `concurrent`<sup>Optional</sup> <a name="cdk-gitlab.HelmRunnerOptions.property.concurrent"></a>

```typescript
public readonly concurrent: number;
```

- *Type:* `number`
- *Default:* 10

Number of run job in the same time.

---

##### `gitlabURL`<sup>Optional</sup> <a name="cdk-gitlab.HelmRunnerOptions.property.gitlabURL"></a>

```typescript
public readonly gitlabURL: string;
```

- *Type:* `string`
- *Default:* 'https://gitlab.com'

gitlab URL prefix.

---

##### `jobDefaultImage`<sup>Optional</sup> <a name="cdk-gitlab.HelmRunnerOptions.property.jobDefaultImage"></a>

```typescript
public readonly jobDefaultImage: string;
```

- *Type:* `string`
- *Default:* alpine:3.11

Gitlab runners default image when job start not set "image" in gitlab-ci.yaml.

---

##### `namespace`<sup>Optional</sup> <a name="cdk-gitlab.HelmRunnerOptions.property.namespace"></a>

```typescript
public readonly namespace: string;
```

- *Type:* `string`
- *Default:* default.

Gitlab helm chart install namespace.

if you change this to other namespace, please addFargateProfile() add that you want namespace.

---

##### `registrationToken`<sup>Optional</sup> <a name="cdk-gitlab.HelmRunnerOptions.property.registrationToken"></a>

```typescript
public readonly registrationToken: string;
```

- *Type:* `string`

GitLab registration token for the runner, you put registrationToken in cdk.context.json like "GITLAB_REGISTRATION_TOKEN": "xxxxxxx".

---

##### `tags`<sup>Optional</sup> <a name="cdk-gitlab.HelmRunnerOptions.property.tags"></a>

```typescript
public readonly tags: string[];
```

- *Type:* `string`[]
- *Default:* ['eks', 'fargate', 'runner']

tags for the runner.

---

### ProviderProps <a name="cdk-gitlab.ProviderProps"></a>

#### Initializer <a name="[object Object].Initializer"></a>

```typescript
import { ProviderProps } from 'cdk-gitlab'

const providerProps: ProviderProps = { ... }
```

##### `vpc`<sup>Optional</sup> <a name="cdk-gitlab.ProviderProps.property.vpc"></a>

```typescript
public readonly vpc: IVpc;
```

- *Type:* [`@aws-cdk/aws-ec2.IVpc`](#@aws-cdk/aws-ec2.IVpc)

---

### RoleProps <a name="cdk-gitlab.RoleProps"></a>

#### Initializer <a name="[object Object].Initializer"></a>

```typescript
import { RoleProps } from 'cdk-gitlab'

const roleProps: RoleProps = { ... }
```

##### `accountId`<sup>Required</sup> <a name="cdk-gitlab.RoleProps.property.accountId"></a>

```typescript
public readonly accountId: string;
```

- *Type:* `string`

---

##### `externalId`<sup>Required</sup> <a name="cdk-gitlab.RoleProps.property.externalId"></a>

```typescript
public readonly externalId: string;
```

- *Type:* `string`

---

## Classes <a name="Classes"></a>

### JobExecutorImage <a name="cdk-gitlab.JobExecutorImage"></a>

The docker image for the job executor.


#### Static Functions <a name="Static Functions"></a>

##### `of` <a name="cdk-gitlab.JobExecutorImage.of"></a>

```typescript
import { JobExecutorImage } from 'cdk-gitlab'

JobExecutorImage.of(image: string)
```

###### `image`<sup>Required</sup> <a name="cdk-gitlab.JobExecutorImage.parameter.image"></a>

- *Type:* `string`

custom image registry URI.

---

#### Properties <a name="Properties"></a>

##### `uri`<sup>Required</sup> <a name="cdk-gitlab.JobExecutorImage.property.uri"></a>

```typescript
public readonly uri: string;
```

- *Type:* `string`

---

#### Constants <a name="Constants"></a>

##### `DEBIAN` <a name="cdk-gitlab.JobExecutorImage.property.DEBIAN"></a>

- *Type:* [`cdk-gitlab.JobExecutorImage`](#cdk-gitlab.JobExecutorImage)

Debian.

> https://gitlab.com/tmaczukin-test-projects/fargate-driver-debian

---

##### `JSII` <a name="cdk-gitlab.JobExecutorImage.property.JSII"></a>

- *Type:* [`cdk-gitlab.JobExecutorImage`](#cdk-gitlab.JobExecutorImage)

JSII for AWS CDK.

> https://gitlab.com/pahud/docker-jsii-cdk-gitlab-ci-fargate

---

##### `NODE` <a name="cdk-gitlab.JobExecutorImage.property.NODE"></a>

- *Type:* [`cdk-gitlab.JobExecutorImage`](#cdk-gitlab.JobExecutorImage)

Node.

> https://gitlab.com/aws-fargate-driver-demo/docker-nodejs-gitlab-ci-fargate

---


## Enums <a name="Enums"></a>

### FargateCapacityProviderType <a name="FargateCapacityProviderType"></a>

Amazon ECS Capacity Providers for AWS Fargate.

#### `FARGATE` <a name="cdk-gitlab.FargateCapacityProviderType.FARGATE"></a>

---


#### `FARGATE_SPOT` <a name="cdk-gitlab.FargateCapacityProviderType.FARGATE_SPOT"></a>

---

