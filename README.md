# pail-credential-gcloud

A [pail](https://pail.build) credential provider: your gcloud login (gcloud auth print-access-token).

```sh
pail auth install gcloud
pail auth use gcloud --for gs://your-bucket --global
```

pail credential provider: your gcloud login (`gcloud auth login`), no application-default
credentials needed. The token carries all of your account's access; for a token limited to
one repository, use gcs-downscoped (or a broker).

It speaks `pail-credential/1`: `pail-credential-gcloud get` reads `{"protocol","store","scheme"}` on stdin and prints
`{"token","expires_at"}`. `pail-extension.json` tells `pail auth install` which file to install.

## License

MIT. See [LICENSE](LICENSE).
