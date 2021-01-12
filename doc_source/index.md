# Amazon Simple Storage Service User Guide

-----
*****Copyright &copy; 2020 Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in 
     connection with any product or service that is not Amazon's, 
     in any manner that is likely to cause confusion among customers, 
     or in any manner that disparages or discredits Amazon. All other 
     trademarks not owned by Amazon are the property of their respective
     owners, who may or may not be affiliated with, connected to, or 
     sponsored by Amazon.

-----
## Contents
+ [What is Amazon S3?](Welcome.md)
+ [Getting started with Amazon S3](GetStartedWithS3.md)
   + [Prerequisite: Setting up Amazon S3](setting-up-s3.md)
   + [Step 1: Create your first S3 bucket](creating-bucket.md)
   + [Step 2: Upload an object to your bucket](uploading-an-object-bucket.md)
   + [Step 3: Download an object](accessing-an-object.md)
   + [Step 4: Copy your object to a folder](copying-an-object.md)
   + [Step 5: Delete your objects and bucket](deleting-object-bucket.md)
   + [How do I change the language of the AWS Management Console?](change-ui-language.md)
   + [Access control best practices](access-control-best-practices.md)
+ [Creating, configuring, and working with Amazon S3 buckets](creating-buckets-s3.md)
   + [Buckets overview](UsingBucket.md)
   + [Bucket naming rules](bucketnamingrules.md)
   + [Creating a bucket](create-bucket-overview.md)
   + [Viewing the properties for an S3 bucket](view-bucket-properties.md)
   + [Accessing a bucket](access-bucket-intro.md)
   + [Emptying a bucket](empty-bucket.md)
   + [Deleting a bucket](delete-bucket.md)
   + [Setting default server-side encryption behavior for Amazon S3 buckets](bucket-encryption.md)
      + [Enabling Amazon S3 default bucket encryption](default-bucket-encryption.md)
      + [Monitoring default encryption with CloudTrail and CloudWatch](bucket-encryption-tracking.md)
   + [Configuring fast, secure file transfers using Amazon S3 Transfer Acceleration](transfer-acceleration.md)
      + [Getting started with Amazon S3 Transfer Acceleration](transfer-acceleration-getting-started.md)
      + [Enabling and using S3 Transfer Acceleration](transfer-acceleration-examples.md)
   + [Configuring Requester Pays buckets for storage transfers and usage](RequesterPaysBuckets.md)
      + [Enabling Requester Pays on a bucket](RequesterPaysExamples.md)
   + [Bucket restrictions and limitations](BucketRestrictions.md)
+ [Uploading, downloading, and working with objects in Amazon S3](uploading-downloading-objects.md)
   + [Amazon S3 objects overview](UsingObjects.md)
   + [Creating object key names](object-keys.md)
   + [Working with object metadata](UsingMetadata.md)
   + [Uploading objects](upload-objects.md)
   + [Uploading and copying objects using multipart upload](mpuoverview.md)
      + [Uploading an object using multipart upload](mpu-upload-object.md)
      + [Listing multipart uploads](list-mpu.md)
      + [Tracking a multipart upload](track-mpu.md)
      + [Aborting a multipart upload](abort-mpu.md)
      + [Copying an object using multipart upload](CopyingObjctsMPUapi.md)
      + [Amazon S3 multipart upload limits](qfacts.md)
   + [Copying objects](copy-object.md)
   + [Downloading an object](download-objects.md)
   + [Deleting Amazon S3 objects](DeletingObjects.md)
      + [Deleting a single object](delete-objects.md)
      + [Deleting multiple objects](delete-multiple-objects.md)
   + [Organizing, listing, and working with your objects](organizing-objects.md)
      + [Organizing objects using prefixes](using-prefixes.md)
      + [Listing object keys programmatically](ListingKeysUsingAPIs.md)
      + [Organizing objects in the Amazon S3 console using folders](using-folders.md)
      + [Viewing an object overview in the Amazon S3 console](view-object-overview.md)
      + [Viewing object properties in the Amazon S3 console](view-object-properties.md)
   + [Accessing an object using a presigned URL](ShareObjectPreSignedURL.md)
      + [Generating a presigned object URL](generate-presigned-url.md)
      + [Uploading objects using presigned URLs](PresignedUrlUploadObject.md)
   + [Retrieving Amazon S3 objects using BitTorrent](S3Torrent.md)
+ [Amazon S3 Security](security.md)
   + [Data protection in Amazon S3](DataDurability.md)
   + [Protecting data using encryption](UsingEncryption.md)
      + [Protecting data using server-side encryption](serv-side-encryption.md)
         + [Protecting Data Using Server-Side Encryption with CMKs Stored in AWS Key Management Service (SSE-KMS)](UsingKMSEncryption.md)
            + [Specifying server-side encryption with AWS KMS (SSE-KMS)](specifying-kms-encryption.md)
            + [Reducing the cost of SSE-KMS with Amazon S3 Bucket Keys](bucket-key.md)
               + [Configuring your bucket to use an S3 Bucket Key with SSE-KMS for new objects](configuring-bucket-key.md)
               + [Configuring an S3 Bucket Key at the object level using the REST API, AWS SDKs, or AWS CLI](configuring-bucket-key-object.md)
               + [Viewing settings for an S3 Bucket Key](viewing-bucket-key-settings.md)
         + [Protecting data using server-side encryption with Amazon S3-managed encryption keys (SSE-S3)](UsingServerSideEncryption.md)
            + [Specifying Amazon S3 encryption](specifying-s3-encryption.md)
         + [Protecting data using server-side encryption with customer-provided encryption keys (SSE-C)](ServerSideEncryptionCustomerKeys.md)
            + [Specifying server-side encryption with customer-provided keys (SSE-C)](specifying-s3-c-encryption.md)
      + [Protecting data using client-side encryption](UsingClientSideEncryption.md)
   + [Internetwork traffic privacy](inter-network-traffic-privacy.md)
   + [Identity and access management in Amazon S3](s3-access-control.md)
      + [Overview of managing access](access-control-overview.md)
      + [Access policy guidelines](access-policy-alternatives-guidelines.md)
      + [How Amazon S3 authorizes a request](how-s3-evaluates-access-control.md)
         + [How Amazon S3 authorizes a request for a bucket operation](access-control-auth-workflow-bucket-operation.md)
         + [How Amazon S3 authorizes a request for an object operation](access-control-auth-workflow-object-operation.md)
      + [Bucket policies and user policies](using-iam-policies.md)
         + [Amazon S3 resources](s3-arn-format.md)
            + [Principals](s3-bucket-user-policy-specifying-principal-intro.md)
            + [Amazon S3 actions](using-with-s3-actions.md)
            + [Amazon S3 condition keys](amazon-s3-policy-keys.md)
            + [Actions, resources, and condition keys for Amazon S3](list_amazons3.md)
         + [Adding a bucket policy using the Amazon S3 console](add-bucket-policy.md)
         + [Controlling access from VPC endpoints with bucket policies](example-bucket-policies-vpc-endpoint.md)
         + [Controlling access to a bucket with user policies](walkthrough1.md)
         + [Bucket policy examples](example-bucket-policies.md)
         + [User policy examples](example-policies-s3.md)
         + [Using service-linked roles for Amazon S3 Storage Lens](using-service-linked-roles.md)
      + [Managing access with ACLs](acl-overview.md)
         + [Access control list (ACL) overview](acl_overview.md)
         + [Configuring ACLs](managing-acls.md)
      + [Configuring and using cross-origin resource sharing (CORS)](cors.md)
         + [Enabling cross-origin resource sharing (CORS)](ManageCorsUsing.md)
         + [Troubleshooting CORS](cors-troubleshooting.md)
      + [Blocking public access to your Amazon S3 storage](access-control-block-public-access.md)
         + [Configuring block public access settings for your account](configuring-block-public-access-account.md)
         + [Configuring block public access settings for your S3 buckets](configuring-block-public-access-bucket.md)
      + [Managing data access with Amazon S3 access points](access-points.md)
         + [Creating access points](creating-access-points.md)
         + [Configuring IAM policies for using access points](access-points-policies.md)
         + [Managing and using access points](using-access-points.md)
            + [Managing and using Amazon S3 access points in the Amazon S3 console](access-points-manage.md)
            + [Using access points with compatible Amazon S3 operations](access-points-usage-examples.md)
         + [Access points restrictions and limitations](access-points-restrictions-limitations.md)
      + [Reviewing bucket access using Access Analyzer for S3](access-analyzer.md)
      + [Controlling object ownership of uploaded objects using S3 Object Ownership](about-object-ownership.md)
      + [Verifying bucket ownership with bucket owner condition](bucket-owner-condition.md)
      + [Example walkthroughs: Managing access to your Amazon S3 resources](example-walkthroughs-managing-access.md)
         + [Example 1: Bucket owner granting its users bucket permissions](example-walkthroughs-managing-access-example1.md)
         + [Example 2: Bucket owner granting cross-account bucket permissions](example-walkthroughs-managing-access-example2.md)
         + [Example 3: Bucket owner granting its users permissions to objects it does not own](example-walkthroughs-managing-access-example3.md)
         + [Example 4: Bucket owner granting cross-account permission to objects it does not own](example-walkthroughs-managing-access-example4.md)
   + [Logging and monitoring in Amazon S3](s3-incident-response.md)
   + [Compliance Validation for Amazon S3](s3-compliance.md)
   + [Resilience in Amazon S3](disaster-recovery-resiliency.md)
   + [Infrastructure security in Amazon S3](network-isolation.md)
   + [Configuration and vulnerability analysis in Amazon S3](vulnerability-analysis-and-management.md)
   + [Security Best Practices for Amazon S3](security-best-practices.md)
+ [Managing your Amazon S3 storage](managing-storage.md)
   + [Using versioning in S3 buckets](Versioning.md)
      + [How S3 Versioning works](versioning-workflows.md)
      + [Enabling versioning on buckets](manage-versioning-examples.md)
      + [Configuring MFA delete](MultiFactorAuthenticationDelete.md)
      + [Working with objects in a versioning-enabled bucket](manage-objects-versioned-bucket.md)
         + [Adding objects to versioning-enabled buckets](AddingObjectstoVersioningEnabledBuckets.md)
         + [Listing objects in a versioning-enabled bucket](list-obj-version-enabled-bucket.md)
         + [Retrieving object versions from a versioning-enabled bucket](RetrievingObjectVersions.md)
         + [Deleting object versions from a versioning-enabled bucket](DeletingObjectVersions.md)
         + [Working with delete markers](DeleteMarker.md)
         + [Deleting an object from an MFA delete-enabled bucket](UsingMFADelete.md)
         + [Configuring versioned object permissions](VersionedObjectPermissionsandACLs.md)
      + [Working with objects in a versioning-suspended bucket](VersionSuspendedBehavior.md)
         + [Adding objects to versioning-suspended buckets](AddingObjectstoVersionSuspendedBuckets.md)
         + [Retrieving objects from versioning-suspended buckets](RetrievingObjectsfromVersioningSuspendedBuckets.md)
         + [Deleting objects from versioning-suspended buckets](DeletingObjectsfromVersioningSuspendedBuckets.md)
      + [Working with archived objects](restoring-objects.md)
         + [Archive retrieval options](restoring-objects-retrieval-options.md)
         + [Restoring an archived object](restoring-objects-console.md)
         + [Querying archived objects](querying-glacier-archives.md)
   + [Using S3 Object Lock](object-lock.md)
      + [S3 Object Lock overview](object-lock-overview.md)
      + [Configuring S3 Object Lock using the S3 console](object-lock-console.md)
      + [Managing Amazon S3 object locks](object-lock-managing.md)
   + [Using Amazon S3 storage classes](storage-class-intro.md)
   + [Managing your storage lifecycle](object-lifecycle-mgmt.md)
      + [Transitioning objects using Amazon S3 Lifecycle](lifecycle-transition-general-considerations.md)
      + [Expiring objects](lifecycle-expire-general-considerations.md)
      + [Using lifecycle with other bucket configurations](lifecycle-and-other-bucket-config.md)
      + [Lifecycle configuration elements](intro-lifecycle-rules.md)
      + [Setting lifecycle configuration on a bucket](how-to-set-lifecycle-configuration-intro.md)
      + [Examples of lifecycle configuration](lifecycle-configuration-examples.md)
   + [Amazon S3 inventory](storage-inventory.md)
      + [Configuring a new Amazon S3 inventory in the S3 console](configure-inventory.md)
      + [Querying Amazon S3 inventory with Amazon Athena](storage-inventory-athena-query.md)
   + [Replicating objects](replication.md)
      + [What does Amazon S3 replicate?](replication-what-is-isnot-replicated.md)
      + [Setting up replication](replication-how-setup.md)
         + [Replication configuration](replication-add-config.md)
         + [Setting up permissions](setting-repl-config-perm-overview.md)
      + [Walkthroughs: Configuring replication](replication-example-walkthroughs.md)
         + [Configuring replication for source and destination buckets owned by the same account](replication-walkthrough1.md)
         + [Configuring replication for source and destination buckets are owned by different accounts](replication-walkthrough-2.md)
         + [Changing the replica owner for source and destination buckets are owned by different accounts](replication-walkthrough-3.md)
         + [Replicating encrypted objects](replication-walkthrough-4.md)
         + [Replicating objects with S3 Replication Time Control (S3 RTC)](replication-walkthrough-5.md)
         + [Managing replication rules using the Amazon S3 console](disable-replication.md)
      + [Additional replication configurations](replication-additional-configs.md)
         + [Monitoring progress with replication metrics and Amazon S3 event notifications](replication-metrics.md)
            + [Enabling S3 replication metrics](enabling-replication-metrics.md)
            + [Viewing replication metrics using the Amazon S3 console](viewing-replication-metrics.md)
         + [Meeting compliance requirements using S3 Replication Time Control (S3 RTC)](replication-time-control.md)
         + [Replicating delete markers between buckets](delete-marker-replication.md)
         + [Replicating metadata changes with Amazon S3 replica modification sync](replication-for-metadata-changes.md)
         + [Changing the replica owner](replication-change-owner.md)
         + [Replicating objects created with server-side encryption (SSE) using AWS KMS CMKs](replication-config-for-kms-objects.md)
      + [Gettinging replication status information](replication-status.md)
      + [Troubleshooting replication](replication-troubleshoot.md)
      + [Additional considerations](replication-and-other-bucket-configs.md)
   + [Categorizing your storage using tags](object-tagging.md)
      + [Managing object tags](tagging-managing.md)
   + [Using cost allocation S3 bucket tags](CostAllocTagging.md)
      + [Billing and usage reporting for S3 buckets](BucketBilling.md)
         + [AWS Billing reports for Amazon S3](aws-billing-reports.md)
         + [AWS usage report for Amazon S3](aws-usage-report.md)
         + [Understanding your AWS billing and usage reports for Amazon S3](aws-usage-report-understand.md)
   + [Filtering and retrieving data using Amazon S3 Select](selecting-content-from-objects.md)
      + [Selecting content from objects](using-select.md)
      + [SQL reference for Amazon S3 Select and S3 Glacier Select](s3-glacier-select-sql-reference.md)
         + [SELECT Command](s3-glacier-select-sql-reference-select.md)
         + [Data Types](s3-glacier-select-sql-reference-data-types.md)
         + [Operators](s3-glacier-select-sql-reference-operators.md)
         + [Reserved Keywords](s3-glacier-select-sql-reference-keyword-list.md)
         + [SQL Functions](s3-glacier-select-sql-reference-sql-functions.md)
            + [Aggregate Functions (Amazon S3 Select only)](s3-glacier-select-sql-reference-aggregate.md)
            + [Conditional Functions](s3-glacier-select-sql-reference-conditional.md)
            + [Conversion Functions](s3-glacier-select-sql-reference-conversion.md)
            + [Date Functions](s3-glacier-select-sql-reference-date.md)
            + [String Functions](s3-glacier-select-sql-reference-string.md)
   + [Performing S3 Batch Operations](batch-ops.md)
      + [S3 Batch Operations basics](batch-ops-basics.md)
      + [Granting permissions for Amazon S3 Batch Operations](batch-ops-iam-role-policies.md)
      + [Operations](batch-ops-operations.md)
         + [Put object copy](batch-ops-copy-object.md)
         + [Initiate restore object](batch-ops-initiate-restore-object.md)
         + [Invoking a Lambda function from Amazon S3 batch operations](batch-ops-invoke-lambda.md)
         + [Put object ACL](batch-ops-put-object-acl.md)
         + [Put object tagging](batch-ops-put-object-tagging.md)
         + [S3 Object Lock retention date](batch-ops-retention-date.md)
         + [S3 Object Lock legal hold](batch-ops-legal-hold.md)
      + [Creating an S3 Batch Operations job](batch-ops-create-job.md)
      + [Managing S3 Batch Operations jobs](batch-ops-managing-jobs.md)
         + [Managing S3 Batch Operations jobs using the S3 console](batch-ops-manage-jobs.md)
         + [Listing jobs](batch-ops-list-jobs.md)
         + [Viewing job details](batch-ops-job-details.md)
         + [Assigning job priority](batch-ops-job-priority.md)
         + [Tracking job status](batch-ops-job-status.md)
      + [Controlling access and labeling jobs using tags](batch-ops-job-tags.md)
         + [Creating a Batch Operations job with job tags used for labeling](batch-ops-tags-create.md)
         + [Deleting the tags from an S3 Batch Operations job](delete-job-tags.md)
         + [Putting job tags for an existing S3 Batch Operations job](put-job-tags.md)
         + [Getting the tags of a S3 Batch Operations job](get-job-tags.md)
         + [Controlling permissions for S3 Batch Operations using job tags](batch-ops-job-tags-examples.md)
      + [Managing S3 Object Lock using S3 Batch Operations](managing-object-lock-batchops.md)
         + [Enabling S3 Object Lock using S3 Batch Operations](batch-ops-object-lock.md)
         + [Setting Object Lock retention using Batch Operations](batch-ops-object-lock-retention.md)
         + [Use S3 Batch Operations with S3 Object Lock retention compliance mode](batch-ops-compliance-mode.md)
         + [Use S3 Batch Operations with S3 Object Lock retention governance mode](batch-ops-governance-mode.md)
         + [Use S3 Batch Operations to turn off S3 Object Lock legal hold](batch-ops-legal-hold-off.md)
      + [Copying objects across AWS accounts using S3 Batch Operations](batch-ops-examples-xcopy.md)
      + [Tracking an S3 Batch Operations job in Amazon EventBridge through AWS CloudTrail](batch-ops-examples-event-bridge-cloud-trail.md)
      + [S3 Batch Operations completion reports](batch-ops-examples-reports.md)
+ [Monitoring Amazon S3](monitoring-overview.md)
   + [Monitoring tools](monitoring-automated-manual.md)
   + [Logging with Amazon S3](logging-with-S3.md)
   + [Logging Amazon S3 API calls using AWS CloudTrail](cloudtrail-logging.md)
      + [Amazon S3 CloudTrail Events](cloudtrail-logging-s3-info.md)
      + [CloudTrail log file entries for Amazon S3 and Amazon S3 on Outposts](cloudtrail-logging-understanding-s3-entries.md)
      + [Enabling CloudTrail event logging for S3 buckets and objects](enable-cloudtrail-logging-for-s3.md)
      + [Identifying Amazon S3 requests using CloudTrail](cloudtrail-request-identification.md)
         + [Identifying requests made to Amazon S3 in a CloudTrail log](identify-S3-requests-using-in-CTlog.md)
         + [Using AWS CloudTrail to identify Amazon S3 signature version 2 requests](cloudtrail-identification-sigv2-requests.md)
         + [Using AWS CloudTrail to identify access to Amazon S3 objects](cloudtrail-identification-object-access.md)
   + [Logging requests with server access logging](ServerLogs.md)
      + [Enabling Amazon S3 server access logging](enable-server-access-logging.md)
      + [Deleting Amazon S3 log files](deleting-log-files-lifecycle.md)
      + [Amazon S3 Server Access Log Format](LogFormat.md)
      + [Using Amazon S3 access logs to identify requests](using-s3-access-logs-to-identify-requests.md)
         + [Querying Amazon S3 access logs for requests using Amazon Athena](querying-s3-access-logs-for-requests.md)
         + [Using Amazon S3 access logs to identify signature version 2 requests](using-s3-access-logs-to-identify-sigv2-requests.md)
   + [Monitoring metrics with Amazon CloudWatch](cloudwatch-monitoring.md)
      + [Metrics and dimensions](metrics-dimensions.md)
      + [Accessing CloudWatch metrics](cloudwatch-monitoring-accessing.md)
      + [Creating a metrics configuration](metrics-configurations.md)
         + [Creating a CloudWatch metrics configuration for all the objects in your bucket](configure-request-metrics-bucket.md)
         + [Creating a metrics configuration that filters by object key name prefix or tag](metrics-configurations-filter.md)
         + [Deleting a metrics filter](delete-request-metrics-filter.md)
   + [Configuring Amazon S3 event notifications](NotificationHowTo.md)
      + [Overview of notifications](notification-how-to-overview.md)
      + [Notification configuration](event-notification-configuration.md)
      + [Event notification types and destinations](notification-how-to-event-types-and-destinations.title.md)
      + [Configuring notifications with object key name filtering](notification-how-to-filtering.md)
      + [Granting permissions to publish event notification messages to a destination](grant-destinations-permissions-to-s3.md)
      + [Walkthrough: Configuring a bucket for notifications (SNS topic or SQS queue)](ways-to-add-notification-config-to-bucket.md)
      + [Enabling and configuring event notifications using the Amazon S3 console](enable-event-notifications.md)
      + [Event message structure](notification-content-structure.md)
+ [Using analytics and insights](analytics-insights.md)
   + [Amazon S3 analytics – Storage Class Analysis](analytics-storage-class.md)
      + [Configuring storage class analysis](configure-analytics-storage-class.md)
   + [Assessing your storage activity and usage with Amazon S3 Storage Lens](storage_lens.md)
      + [Understanding Amazon S3 Storage Lens](storage_lens_basics_metrics_recommendations.md)
      + [Using Amazon S3 Storage Lens with AWS Organizations](storage_lens_with_organizations.md)
      + [Setting permissions to use Amazon S3 Storage Lens](storage_lens_iam_permissions.md)
      + [Viewing storage usage and activity metrics with Amazon S3 Storage Lens](storage_lens_view_metrics.md)
         + [Viewing S3 Storage Lens metrics on the dashboards](storage_lens_view_metrics_dashboard.md)
         + [Viewing Amazon S3 Storage Lens metrics using a data export](storage_lens_view_metrics_export.md)
            + [Using an AWS KMS CMK to encrypt your metrics exports](storage_lens_encrypt_permissions.md)
            + [What is an S3 Storage Lens export manifest?](storage_lens_whatis_metrics_export_manifest.md)
            + [Understanding the Amazon S3 Storage Lens export schema](storage_lens_understanding_metrics_export_schema.md)
      + [Amazon S3 Storage Lens metrics glossary](storage_lens_metrics_glossary.md)
      + [Amazon S3 Storage Lens examples and console walk-through](S3LensExamples.md)
         + [Using Amazon S3 Storage Lens in the console](storage_lens_console.md)
            + [Viewing an Amazon S3 Storage Lens dashboard](storage_lens_console_viewing.md)
            + [Creating and updating Amazon S3 Storage Lens dashboards](storage_lens_console_creating_editing.md)
               + [Creating an Amazon S3 Storage Lens dashboard](storage_lens_console_creating.md)
               + [Updating an Amazon S3 Storage Lens dashboard](storage_lens_console_editing.md)
            + [Disabling or deleting Amazon S3 Storage Lens dashboards](storage_lens_console_disabling_deleting.md)
               + [Disabling an Amazon S3 Storage Lens dashboard](storage_lens_console_disabling.md)
               + [Deleting an Amazon S3 Storage Lens dashboard](storage_lens_console_deleting.md)
            + [Working with AWS Organizations to create organization-level dashboards](storage_lens_console_organizations.md)
               + [Enabling trusted access for S3 Storage Lens in your organization](storage_lens_console_organizations_enabling_trusted_access.md)
               + [Disabling S3 Storage Lens trusted access in your organization](storage_lens_console_organizations_disabling_trusted_access.md)
               + [Registering delegated administrators for S3 Storage Lens](storage_lens_console_organizations_registering_delegated_admins.md)
               + [Deregistering delegated administrators for S3 Storage Lens](storage_lens_console_organizations_deregistering_delegated_admins.md)
         + [Amazon S3 Storage Lens examples using the AWS CLI](S3LensCLIExamples.md)
         + [Amazon S3 Storage Lens examples using the SDK for Java](S3LensJavaExamples.md)
   + [Tracing Amazon S3 requests using AWS X-Ray](tracing_requests_using_xray.md)
+ [Hosting a static website using Amazon S3](WebsiteHosting.md)
   + [Website endpoints](WebsiteEndpoints.md)
   + [Enabling website hosting](EnableWebsiteHosting.md)
   + [Configuring an index document](IndexDocumentSupport.md)
   + [Configuring a custom error document](CustomErrorDocSupport.md)
   + [Setting permissions for website access](WebsiteAccessPermissionsReqd.md)
   + [(Optional) Logging web traffic](LoggingWebsiteTraffic.md)
   + [(Optional) Configuring a webpage redirect](how-to-page-redirect.md)
   + [Walkthroughs - Hosting websites on Amazon S3](hosting-websites-on-s3-examples.md)
      + [Tutorial: Configuring a static website on Amazon S3](HostingWebsiteOnS3Setup.md)
      + [Configuring a static website using a custom domain registered with Route 53](website-hosting-custom-domain-walkthrough.md)
         + [Speeding up your website with Amazon CloudFront](website-hosting-cloudfront-walkthrough.md)
         + [Cleaning up your example resources](getting-started-cleanup.md)
+ [Developing with Amazon S3](developing-s3.md)
   + [Making requests](MakingRequests.md)
      + [Making requests to Amazon S3 over IPv6](ipv6-access.md)
         + [Using Amazon S3 dual-stack endpoints](dual-stack-endpoints.md)
      + [Making requests using the AWS SDKs](MakingAuthenticatedRequests.md)
         + [Making requests using AWS account or IAM user credentials](AuthUsingAcctOrUserCredentials.md)
         + [Making requests using IAM user temporary credentials](AuthUsingTempSessionToken.md)
         + [Making requests using federated user temporary credentials](AuthUsingTempFederationToken.md)
      + [Making requests using the REST API](RESTAPI.md)
         + [Virtual hosting of buckets](VirtualHosting.md)
         + [Request redirection and the REST API](RESTRedirect.md)
   + [Developing with Amazon S3 using the AWS CLI](setup-aws-cli.md)
   + [Developing with Amazon S3 using the AWS SDKs, and explorers](UsingAWSSDK.md)
      + [Using the AWS SDK for Java](UsingTheMPJavaAPI.md)
      + [Using the AWS SDK for .NET](UsingTheMPDotNetAPI.md)
      + [Using the AWS SDK for PHP and Running PHP Examples](UsingTheMPphpAPI.md)
      + [Using the AWS SDK for Ruby - Version 3](UsingTheMPRubyAPI.md)
      + [Using the AWS SDK for Python (Boto)](UsingTheBotoAPI.md)
      + [Using the AWS Mobile SDKs for iOS and Android](using-mobile-sdks.md)
      + [Using the AWS Amplify JavaScript Library](using-aws-amplify.md)
   + [Developing with Amazon S3 using the REST API](developing-rest-api.md)
      + [Request routing](UsingRouting.md)
      + [Handling REST and SOAP errors](HandlingErrors.md)
         + [The REST error response](UsingRESTError.md)
         + [Amazon S3 error best practices](ErrorBestPractices.md)
   + [Developer reference](Appendices.md)
      + [Appendix a: Using the SOAP API](SOAPAPI3.md)
         + [Common SOAP API elements](UsingSOAPOperations.md)
         + [Authenticating SOAP requests](SOAPAuthentication.md)
         + [Setting access policy with SOAP](SOAPAccessPolicy.md)
      + [Appendix b: Authenticating requests (AWS signature version 2)](auth-request-sig-v2.md)
         + [Authenticating requests using the REST API](S3_Authentication2.md)
         + [Signing and authenticating REST requests](RESTAuthentication.md)
         + [Browser-based uploads using POST (AWS signature version 2)](UsingHTTPPOST.md)
            + [HTML forms (AWS signature version 2)](HTTPPOSTForms.md)
            + [Upload examples (AWS signature version 2)](HTTPPOSTExamples.md)
            + [POST with adobe flash](HTTPPOSTFlash.md)
+ [Best practices design patterns: optimizing Amazon S3 performance](optimizing-performance.md)
   + [Performance Guidelines for Amazon S3](optimizing-performance-guidelines.md)
   + [Performance Design Patterns for Amazon S3](optimizing-performance-design-patterns.md)
+ [Using Amazon S3 on Outposts](S3onOutposts.md)
   + [Getting started with Amazon S3 on Outposts](S3OutpostsGS.md)
   + [Amazon S3 on Outposts restrictions and limitations](S3OnOutpostsRestrictionsLimitations.md)
   + [Using AWS Identity and Access Management with Amazon S3 on Outposts](S3OutpostsIAM.md)
   + [Working with Amazon S3 on Outposts](WorkingWithS3Outposts.md)
      + [Accessing Amazon S3 on Outposts using virtual private cloud (VPC) only access points](AccessingS3Outposts.md)
      + [Monitoring Amazon S3 on Outposts](MonitoringS3Outposts.md)
   + [Amazon S3 on Outposts examples](S3OutpostsExamples.md)
      + [Amazon S3 on Outposts examples using the AWS CLI](S3OutpostsCLIExamples.md)
      + [Amazon S3 on Outposts examples using the SDK for Java](S3OutpostsJavaExamples.md)
         + [Creating and managing Amazon S3 on Outposts bucket](S3OutpostsBucketJava.md)
         + [Working with objects using Amazon S3 on Outposts](S3OutpostsObjectJava.md)
+ [Troubleshooting](troubleshooting.md)
   + [Troubleshooting Amazon S3 by Symptom](troubleshooting-by-symptom.md)
   + [Getting Amazon S3 Request IDs for AWS Support](get-request-ids.md)
+ [Document History](WhatsNew.md)
+ [AWS glossary](glossary.md)