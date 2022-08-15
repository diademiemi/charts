# BoneBot

![Version: 1.0.0](https://img.shields.io/badge/Version-1.0.0-informational?style=flat-square) ![AppVersion: latest](https://img.shields.io/badge/AppVersion-1.0.0-informational?style=flat-square)

Dropspace helm package

## Source Code

* https://github.com/leventdev/dropspace

## Requirements

Kubernetes: `>=1.16.0-0`

## Dependencies

| Repository | Name | Version |
|------------|------|---------|
| https://library-charts.k8s-at-home.com | common | 4.0.0 |

## TL;DR

```console
helm repo add diademiemi https://diademiemi.github.io/charts
helm repo update
helm install dropspace diademiemi/dropspace
```

## Installing the Chart

To install the chart with the release name `dropspace`

```console
helm install dropspace diademiemi/dropspace
```

## Uninstalling the Chart

To uninstall the `dropspace` deployment

```console
helm uninstall dropspace
```

The command removes all the Kubernetes components associated with the chart **including persistent volumes** and deletes the release.

**Important**: When deploying an application Helm chart you can add more values from our common library chart [here](https://github.com/k8s-at-home/library-charts/tree/main/charts/stable/common)

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env | object | See below | environment variables. See more environment variables in the [bonebot documentation](https://bonebot.org/docs). |
| env.TZ | string | `"UTC"` | Set the container timezone |
| image.pullPolicy | string | `"IfNotPresent"` | image pull policy |
| image.repository | string | `"ghcr.io/diademiemi/bonebot"` | image repository |
| image.tag | string | chart.appVersion | image tag |
| ingress.main | object | See values.yaml | Enable and configure ingress settings for the chart under this key. |
| persistence | object | See values.yaml | Configure persistence settings for the chart under this key. |
| service | object | See values.yaml | Configures service settings for the chart. |

## Changelog

### Version 1.0.0

#### Added

- Initial version

#### Changed

N/A

#### Fixed

N/A

