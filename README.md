# profile

{
"deploymentId" : "infa-model",
"yamlFileContent" : "apiVersion: serving.kserve.io/v1beta1\nkind: InferenceService\nmetadata:\n  name: infa-model\n  labels:\n    id: infa-model\n    orgId: informatica\nspec:\n  predictor:\n    containers:\n      - name: infa-model-container\n        image: hemshankar/infa_custom_model:latest\n        args: [\"--model_name\", \"infa_custom_model\" , \"--dependency_url\", \"https://cdiqa.s3.amazonaws.com/tmp/user_model.zip\"]"
}
