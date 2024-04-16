# LeastNUMANodes ScoringStrategy for NodeResourceTopologyMatch plugin

<!-- toc -->
- [Summary](#summary)
- [Motivation](#motivation)
  - [Goals](#goals)
  - [Non-Goals](#non-goals)
- [Proposal](#proposal)
- [Use cases](#use-cases)
- [Known limitations](#known-limitations)
- [Test plans](#test-plans)
- [Graduation criteria](#graduation-criteria)
- [Production Readiness Review Questionnaire](#production-readiness-review-questionnaire)
  - [Feature enablement and rollback](#feature-enablement-and-rollback)
- [Implementation history](#implementation-history)
<!-- /toc -->

# Summary

This document describes a preemption framework for kube-scheduler. The new preemption framework will 
be coscheduling nativing, which will try to preempt a job a time instead of a single pod, and it will 
support some hook for other plugin to influence the preemption behavior. 

# Motivation

Default preemption will preempt existing pods for one pod a time, but the preemptor may not be able
to start even enough resource were reserved by preemption because pods in podgroup are expected to start 
together. For pods in podgroup, pods are supposed to preempt others only when all unschedulable pods can
get enough resource by preemption. 

## Goals

## Non-Goals

# Proposal

## Preemption framework

New preemption framework will try to preempt for the last pod in a podgroup and any pod not in a podgroup.
For a pod not in a podgroup, 

## How can out-of-tree plugins work with preemption framework

### Example

# Use cases

# Known limitations

# Test plans

# Graduation criteria

# Production Readiness Review Questionnaire

## Feature enablement and rollback

# Implementation history
