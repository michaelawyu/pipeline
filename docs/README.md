---
title: "Tasks and Pipelines"
linkTitle: "Tasks and Pipelines"
weight: 2
description: >
  Building Blocks of Tekton CI/CD Workflow
---

Tekton Pipelines is an open source implementation to configure and run CI/CD
style pipelines for your Kubernetes application.

Pipeline creates
[Custom Resources](https://kubernetes.io/docs/concepts/extend-kubernetes/api-extension/custom-resources/)
as building blocks to declare pipelines.

A custom resource is an extension of Kubernetes API which can create a custom
[Kubernetes Object](https://kubernetes.io/docs/concepts/overview/working-with-objects/kubernetes-objects/#understanding-kubernetes-objects).
Once a custom resource is installed, users can create and access its objects
with kubectl, just as they do for built-in resources like pods, deployments etc.
These resources run on-cluster and are implemented by
[Kubernetes Custom Resource Definition (CRD)](https://kubernetes.io/docs/concepts/extend-kubernetes/api-extension/custom-resources/#customresourcedefinitions).

High level details of this design:

- [Pipelines](/docs/pipelines/pipelines) do not know what will trigger them, they can be
  triggered by events or by manually creating [PipelineRuns](/docs/pipelines/pipelineruns)
- [Tasks](/docs/pipelines/tasks) can exist and be invoked completely independently of
  [Pipelines](/docs/pipelines/pipelines); they are highly cohesive and loosely coupled
- [Tasks](/docs/pipelines/tasks) can depend on artifacts and parameters created by other
  tasks.
- [Tasks](/docs/pipelines/tasks) can be invoked via [TaskRuns](/docs/pipelines/taskruns)
- [PipelineResources](/docs/pipelines/resources) are the artifacts used as inputs and outputs
  of Tasks.

## Usage

- [How do I create a new Pipeline?](/docs/pipelines/pipelines)
- [How do I make a Task?](/docs/pipelines/tasks)
- [How do I make Resources?](/docs/pipelines/resources)
- [How do I control auth?](/docs/pipelines/auth)
- [How do I run a Pipeline?](/docs/pipelines/pipelineruns)
- [How do I run a Task on its own?](/docs/pipelines/taskruns)
- [How do I get logs?](/docs/pipelines/logs)

## Learn more

See the following reference topics for information about each of the build
components:

- [`Task`](/docs/pipelines/tasks)
- [`TaskRun`](/docs/pipelines/taskruns)
- [`Pipeline`](/docs/pipelines/pipelines)
- [`PipelineRun`](/docs/pipelines/pipelineruns)
- [`PipelineResource`](/docs/pipelines/resources)

Additional reference topics not related to a specific component:

- [Labels](/docs/pipelines/labels)
- [Logs](/docs/pipelines/logs)

## Try it out

- Follow along with [the tutorial](https://github.com/tektoncd/pipeline/blob/master/docs/tutorial.md)
- Look at
  [the examples](https://github.com/tektoncd/pipeline/tree/master/examples)

## Related info

If you are interested in contributing to the Tekton Pipeline project, see the
[Tekton Pipeline contribution guide](https://github.com/tektoncd/pipeline/blob/master/CONTRIBUTING.md).

---

Except as otherwise noted, the content of this page is licensed under the
[Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/),
and code samples are licensed under the
[Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0).
