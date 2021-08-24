# GitHub Action - AWS Lambda Layer Publish with compatible runtime
![GitHub release (latest by date)](https://img.shields.io/github/v/release/killdozerx2/aws-lambda-publishlayer)  [![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)

Deploy a layer to aws lambda

# Usage

## Secrets

Add Secret before this action. `Settings > Secrets > Add a new secret`

- `AWS_REGION`
- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`

## Example
```yml
- name: AWS Lambda Layer Publish
  uses: killdozerx2/aws-lambda-publishlayer@v1.0.0
  env:
    AWS_REGION: ${{ secrets.AWS_REGION }}
    AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
    AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
  with:
    layer_name: TargetFunctionName
    zip_file: path/to/file.zip
    description: verbose description of the layer, not required
    compatible_runtimes: An array of compatible runtimes, pass as a string, remember to stringify the array before including it here, not required
```

## Important
This action was forked from [taotao2345/aws-lambda-publishlayer](https://github.com/taotao2345/aws-lambda-publishlayer).  
However, @taotao has not reacted to the pull request and hence this action exists, if you are @taotao or you know @taotao please consider accepting/rejecting the ppull_request.
