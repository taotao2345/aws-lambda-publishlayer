# GitHub Action - AWS Lambda Layer Publish

Run PublishLayerVersion

# Usage

## Secret

Add Secret before this action. `Settings > Secrets > Add a new secret`

- `AWS_REGION`
- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`

## Example
```yml
- name: AWS Lambda Layer Publish
  uses: taotao2345/aws-lambda-publishlayer@v1.0.0
  env:
    AWS_REGION: ${{ secrets.AWS_REGION }}
    AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
    AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
  with:
    layer_name: TargetFunctionName
    zip_file: path/to/file.zip
```
