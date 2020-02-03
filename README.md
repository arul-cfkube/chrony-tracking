# chrony-tracking
This guides is help to track time synchronzation on bosh deployed vms.  The script runs as bosh addon on diego cell to run chroncyc tracking cmd.



# Upload cron release to bosh
```
bosh upload-release --sha1 fc04ff78ff958487be8829bb93d9023f6a87b7e6 \
  https://bosh.io/d/github.com/cloudfoundry-community/cron-boshrelease?v=1.3.0

```

# Upload addon yaml as addon runtime config

```
bosh update-runtime-config chrony-tracking.yml --name chrony-tracking

```


# Deploy using bosh

```
bosh -d deployment deploy cf-manifest.yml

```
