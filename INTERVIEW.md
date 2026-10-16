# Wanderlust deployment lab — fork: reviewer guide

A forked travel-blog application with Docker and Jenkins/GitOps deployment material.

## Start the review

Credit the upstream application and isolate the pipeline, infrastructure, or deployment work you personally changed.

| Source | Review focus |\n| --- | --- |\n| [Jenkinsfile](Jenkinsfile) | Triggers, credentials, failure handling, and deploy conditions |\n| [docker-compose.yml](docker-compose.yml) | Build context, runtime configuration, ports, and persistence |\n| [package.json](package.json) | Implementation, assumptions, and operational boundaries |\n| [terraform/ec2.tf](terraform/ec2.tf) | Inputs, state, permissions, cost, and resource lifecycle |\n| [terraform/terraform.tf](terraform/terraform.tf) | Inputs, state, permissions, cost, and resource lifecycle |\n| [terraform/variables.tf](terraform/variables.tf) | Inputs, state, permissions, cost, and resource lifecycle |

## A useful interview walkthrough

1. State the problem and the specific part you implemented or changed.
2. Open the source above and follow one request, release, or failure from start to finish.
3. Show a reproducible result, including an actual failure and the observation that confirms recovery.
4. Explain one tradeoff and one limitation. Distinguish a local test from a live deployment.

## Evidence and limits

This guide is based on the default-branch source inspected on 16 October 2026. It is a source review, not a fresh deployment or a certification of every feature. Existing CI runs and tests should be checked at the commit being demonstrated. Do not present screenshots, inherited code, planned features, or old README statements as proof of a current deployment.

## Attribution

This repository is a fork of [LondheShubham153/Wanderlust-Mega-Project](https://github.com/LondheShubham153/Wanderlust-Mega-Project). The application and existing documentation retain their original authorship. Use commit diffs to identify any changes made in this fork; no original authorship or completed deployment is implied.
