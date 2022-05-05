# Continuous Access Evaluation - Demo Components

> Demo Content for Continuous Access Evaluation (CAE) and Signal Sharing Event (SSE) framework to enable relying parties to support token revocation without the need to constantly contact token issuers at runtime.

Please refer to the Blog for more details on architecture and context for this CAE demo. 

## Step 1: Install a message Broker and setup queue "revokedTokenQ".

  > I have leveraged Apache ActiveMQ for this demo and please refer to the link below for:
  
1. "Getting Started" https://activemq.apache.org/getting-started.

## Step 2: Deploy Layer7 APIM Gateway with required JMS library for communicating with message Broker.
  > Please refer to the following links for more details on deployment and also JMS configuration:

### 1. Layer7 APIM Deployment in GCP using Helm Charts: 
        a. https://techdocs.broadcom.com/us/en/ca-enterprise-software/layer7-api-management/api-gateway/congw-10-1/install-configure-upgrade.html
        b. https://github.com/CAAPIM/apim-charts
### 2. OAuth Tool Kit COnfiguration
        a. https://techdocs.broadcom.com/us/en/ca-enterprise-software/layer7-api-management/api-management-oauth-toolkit/4-5/installation-workflow.html
### 4. Installing and configuring JMS interface with Gateway:
        a. https://techdocs.broadcom.com/us/en/ca-enterprise-software/layer7-api-management/api-gateway/congw-10-1/security-configuration-in-policy-manager/tasks-menu-security-options/manage-jms-destinations/install-the-jms-interface.html

## Step 3: Using Gateway Migration Utility load the CAE Policy bundle into the gateway: 
  > Enclosed in this repository.
 
 ### 1. Revoke Token Bundle:
        a. https://github.com/bradhakr/CAE.git
 
 
