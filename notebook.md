To launch jupyter notebook pre-installed compute engine
search `Tensorflow` and I use the following
```
AISE TensorFlow NVidia GPU Notebook overview
```
If you get an error like
```
tensorflow-python-cuda-minilab-1-vm: {"ResourceType":"compute.v1.instance","ResourceErrorCode":"QUOTA_EXCEEDED","ResourceErrorMessage":"Quota 'GPUS_ALL_REGIONS' exceeded. Limit: 0.0 globally."}
```

Go to `IAM & Admin` --> `Quotas` 

In `Metric` --> `GPU (All regions)` --> Edit Quotas, increase the limit to `1`, submit the request 

