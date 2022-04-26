# mountainpass/s3cmd

Containerised `s3cmd` command line tool - used for syncing files to/from s3 compatible buckets (e.g. DigitalOcean Spaces).

## Usage

```
# setup
docker run -it --rm -v "$(pwd):/root" mountainpass/s3cmd s3cmd --configure

# run
docker run -it --rm -v "$(pwd):/root" mountainpass/s3cmd s3cmd sync ./yourfolder s3://yourbucket/ \
    --acl-public \
    --add-header=Cache-Control:max-age=3600 \
    --recursive
```

## Build

```
docker build . --tag mountainpass/s3cmd
```
