# Changelog - OpenTelemetry.Contrib.Extensions.AWSXRay

## Unreleased

* Updates to 1.5.1 of OpenTelemetry SDK.
  ([#1255](https://github.com/open-telemetry/opentelemetry-dotnet-contrib/pull/1255))
* Enhancement - AWSXRayIdGenerator - Generate X-Ray IDs with global Random
  instance instead of recreating with ThreadLocal
  ([#380](https://github.com/open-telemetry/opentelemetry-dotnet-contrib/pull/380))
* Raised minimum .NET version to `net462`
  ([#875](https://github.com/open-telemetry/opentelemetry-dotnet-contrib/pull/875))
* Replaced Newtonsoft.Json dependency with System.Text.Json
  ([#1092](https://github.com/open-telemetry/opentelemetry-dotnet-contrib/pull/1092))
* Enhancement - AWSECSResourceDetector - Implement `aws.{ecs.*,log.*}` resource
  attributes with data from ECS Metadata endpoint v4
  ([#875](https://github.com/open-telemetry/opentelemetry-dotnet-contrib/pull/875))
* Removal - IResourceDetector - Remove local IResourceDetector interface and its
  supporting ResourceBuilderExtensions extension, and migrate all detectors to
  implement OpenTelemetry.Resources.IResourceDetector
  ([#875](https://github.com/open-telemetry/opentelemetry-dotnet-contrib/pull/875))
* Drop support for `AWSLambdaResourceDetector`.
  AWS Lambda Resources are detected by `OpenTelemetry.Instrumentation.AWSLambda`
  package
  ([#1140](https://github.com/open-telemetry/opentelemetry-dotnet-contrib/pull/1140))
* Extract AWS Resource Detectors to dedicated package `OpenTelemetry.ResourceDetectors.AWS`
  ([#1140](https://github.com/open-telemetry/opentelemetry-dotnet-contrib/pull/1140))

## 1.2.0

Released 2022-May-18

* Enhancement - AWSEKSResourceDetector - Validate ClusterName/ContainerID
  independently before adding it to the resource
  ([#205](https://github.com/open-telemetry/opentelemetry-dotnet-contrib/pull/205))
* Fix - AWSEKSResourceDetector fails to detect resources due to exception
  "The SSL connection could not be established"
  ([#208](https://github.com/open-telemetry/opentelemetry-dotnet-contrib/pull/208))

## 1.1.0

Released 2021-Sep-20

* Added AWS resource detectors ([#149](https://github.com/open-telemetry/opentelemetry-dotnet-contrib/pull/149))
* Updated OpenTelemetry SDK package version to 1.1.0
  ([#100](https://github.com/open-telemetry/opentelemetry-dotnet-contrib/pull/100))

## 1.0.1

Released 2021-Feb-24

This is the first release for the `OpenTelemetry.Contrib.Extensions.AWSXRay`
project. The project targets v1.0.1 of the [OpenTelemetry
SDK](https://www.nuget.org/packages/OpenTelemetry/).

The AWSXRay extensions include plugin to generate X-Ray format trace-ids and a
propagator to propagate the X-Ray trace header to downstream. For more details,
please refer to the
[README](https://github.com/open-telemetry/opentelemetry-dotnet-contrib/blob/main/src/OpenTelemetry.Contrib.Extensions.AWSXRay/README.md)
