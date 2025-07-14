
# Retail Demo Store

The Retail Demo Store is an eCommerce reference implementation designed to showcase how AWS services can be used to build compelling shopping experiences using modern architecture and design patterns.

> [!IMPORTANT]  
> The documentation is now supported by [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) 
>
> You can read directly on github [https://aws-samples.github.io/retail-demo-store/](https://aws-samples.github.io/retail-demo-store/)
>


> [!NOTE]
> Jump directly to a section of the documentation:
>
> * [How to deploy an instance in your account ](https://aws-samples.github.io/retail-demo-store/Deployment/getting-started/)
> * [Hands-on Workshops](https://aws-samples.github.io/retail-demo-store/workshops/hands-on-workshops/)
> * [Partner Integrations](https://aws-samples.github.io/retail-demo-store/partner-integrations/partner-integrations/)
> * [Delivering a Demo of the Retail Demo Store](https://aws-samples.github.io/retail-demo-store/Available%20Demos/)
> * [Troubleshooting - FAQs](https://aws-samples.github.io/retail-demo-store/Deployment/troubleshooting/)


**This project is intended for educational purposes only and not for production use.**

![Retail Demo Store Home Page](./docs/assets/retaildemostore-home-devices.png)


## Build Status

![Ruff](https://github.com/aws-samples/retail-demo-store/actions/workflows/ruff.yml/badge.svg?branch=master)
![UI Build](https://github.com/aws-samples/retail-demo-store/actions/workflows/build-ui.yml/badge.svg?branch=master)

build fix commands
sudo apt-get update
sudo apt-get install python3-venv
rm -rf .venv
./stage.sh retail-demo-store-staging--environment-qa retail-demo-store-artifacts/
python3 --version
python3 -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r generators/requirements.txt
./stage.sh retail-demo-store-staging--environment-qa retail-demo-store-artifacts/
sudo shutdown +30

stack creation


aws cloudformation create-stack   --stack-name retaildemostore   --template-url https://s3.eu-west-1.amazonaws.com/retail-demo-store-staging--environment-qa/retail-demo-store-artifacts/cloudformation-templates/template.yaml   --region eu-west-1   --capabilities CAPABILITY_IAM CAPABILITY_NAMED_IAM CAPABILITY_AUTO_EXPAND   --parameters     ParameterKey=ResourceBucket,ParameterValue=retail-demo-store-staging--environment-qa     ParameterKey=ResourceBucketRelativePath,ParameterValue=retail-demo-store-artifacts/     ParameterKey=CreateOpenSearchServiceLinkedRole,ParameterValue=Yes     ParameterKey=SourceDeploymentType,ParameterValue=S3     ParameterKey=GitHubRepo,ParameterValue=retail-demo-store     ParameterKey=GitHubBranch,ParameterValue=master     ParameterKey=GitHubUser,ParameterValue=aws-samples     ParameterKey=PreIndexOpenSearch,ParameterValue=No     ParameterKey=PreCreatePersonalizeResources,ParameterValue=No     ParameterKey=PreCreatePinpointWorkshop,ParameterValue=No     ParameterKey=UseDefaultIVSStreams,ParameterValue=Yes     ParameterKey=DeployLocationServices,ParameterValue=Yes     ParameterKey=DeployPersonalizedOffersCampaign,ParameterValue=Yes     ParameterKey=BedrockProductPersonalization,ParameterValue=No     ParameterKey=DeployRoomMakeoverDemo,ParameterValue=No     ParameterKey=EnableSageMakerAutoScaling,ParameterValue=Yes     ParameterKey=SageMakerScalingMinCapacity,ParameterValue=0     ParameterKey=SageMakerScalingMaxCapacity,ParameterValue=1     ParameterKey=SageMakerEndpointName,ParameterValue=controlnet-depth-sdxl     ParameterKey=OpenSearchEmbeddingIndex,ParameterValue=embproducts     ParameterKey=FenixZipDetectUrl,ParameterValue=https://ipapi.co/json?key=cKGC3jQbSIoXYmI2KtXObugsKfosD9Yr0HnkHhPUu1SM2wQhE0     ParameterKey=FenixEddEndpoint,ParameterValue=https://platform.api.fenixcommerce.com/awsretaildemostore/fenixdelest/api/v2/deliveryestimates     ParameterKey=FenixMonetaryValue,ParameterValue=100     ParameterKey=FenixEnabledPdp,ParameterValue=FALSE     ParameterKey=FenixEnabledCart,ParameterValue=FALSE     ParameterKey=FenixEnabledCheckout,ParameterValue=FALSE

aws cloudformation create-stack   --stack-name retaildemostore   --template-url https://s3.eu-west-1.amazonaws.com/retail-demo-store-staging--environment-qa/retail-demo-store-artifacts/cloudformation-templates/template.yaml   --region eu-west-1   --capabilities CAPABILITY_IAM CAPABILITY_NAMED_IAM CAPABILITY_AUTO_EXPAND   --parameters     ParameterKey=ResourceBucket,ParameterValue=retail-demo-store-staging--environment-qa     ParameterKey=ResourceBucketRelativePath,ParameterValue=retail-demo-store-artifacts/     ParameterKey=CreateOpenSearchServiceLinkedRole,ParameterValue=Yes     ParameterKey=SourceDeploymentType,ParameterValue=S3     ParameterKey=GitHubRepo,ParameterValue=retail-demo-store     ParameterKey=GitHubBranch,ParameterValue=master     ParameterKey=GitHubUser,ParameterValue=aws-samples     ParameterKey=PreIndexOpenSearch,ParameterValue=No     ParameterKey=PreCreatePersonalizeResources,ParameterValue=No     ParameterKey=PreCreatePinpointWorkshop,ParameterValue=No     ParameterKey=UseDefaultIVSStreams,ParameterValue=Yes     ParameterKey=DeployLocationServices,ParameterValue=Yes     ParameterKey=DeployPersonalizedOffersCampaign,ParameterValue=Yes     ParameterKey=BedrockProductPersonalization,ParameterValue=No     ParameterKey=DeployRoomMakeoverDemo,ParameterValue=No     ParameterKey=EnableSageMakerAutoScaling,ParameterValue=Yes     ParameterKey=SageMakerScalingMinCapacity,ParameterValue=0     ParameterKey=SageMakerScalingMaxCapacity,ParameterValue=1     ParameterKey=SageMakerEndpointName,ParameterValue=controlnet-depth-sdxl     ParameterKey=OpenSearchEmbeddingIndex,ParameterValue=embproducts     ParameterKey=FenixZipDetectUrl,ParameterValue=https://ipapi.co/json?key=cKGC3jQbSIoXYmI2KtXObugsKfosD9Yr0HnkHhPUu1SM2wQhE0     ParameterKey=FenixEddEndpoint,ParameterValue=https://platform.api.fenixcommerce.com/awsretaildemostore/fenixdelest/api/v2/deliveryestimates     ParameterKey=FenixMonetaryValue,ParameterValue=100     ParameterKey=FenixEnabledPdp,ParameterValue=FALSE     ParameterKey=FenixEnabledCart,ParameterValue=FALSE     ParameterKey=FenixEnabledCheckout,ParameterValue=FALSE
