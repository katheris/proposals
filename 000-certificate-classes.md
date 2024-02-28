<!-- This template is provided as an example with sections you may wish to comment on with respect to your proposal. Add or remove sections as required to best articulate the proposal. -->

# <Title>

Provide a brief summary of the feature you are proposing to add to Strimzi.

## Current situation

Currently, Strimzi uses the following classes to encapsulate the use of certificates:

| Class name | Type | Purpose | Implemented By | Used By |
| io.strimzi.certs.CertManager | interface | Manages certificates, e.g. generating, signing etc | OpenSslCertManager, MockCertManager (for testing) | Ca, KafkaAssemblyOperator, KafkaMirrorMakerAssemblyOperator, KafkaBridgeAssemblyOperator, CaReconciler |
| io.strimzi.operator.common.model.Ca | abstract class | Certificate Authority which can renew its own (self-signed) certificates and generate signed certificates | ClusterCa, ClientCa | ResourceUtils, CertUtils, ModelUtils, CaReconciler, CruiseControlReconciler, EntityOperatorReconciler, KafkaExporterReconciler, KafkaReconciler, ReconcilerUtils, ZooKeeperReconciler, ZookeeperLeaderFinder, ZookeeperScaler |


## Motivation

Explain the motivation why this should be added, and what value it brings.

## Proposal

Provide an introduction to the proposal. Use sub sections to call out considerations, possible delivery mechanisms etc.

## Affected/not affected projects

Call out the projects in the Strimzi organisation that are/are not affected by this proposal. 

## Compatibility

Call out any future or backwards compatibility considerations this proposal has accounted for.

## Rejected alternatives

Call out options that were considered while creating this proposal, but then later rejected, along with reasons why.
