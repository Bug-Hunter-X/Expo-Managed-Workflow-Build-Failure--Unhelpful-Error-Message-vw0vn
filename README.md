# Expo Managed Workflow Build Failure: Unhelpful Error Message

This repository demonstrates a bug in the Expo managed workflow where a build fails with an unhelpful error message when there's an issue with loading assets. The error message does not provide enough information to debug, and even adding the missing asset does not resolve the issue.

## Bug Description

A simple Expo app that attempts to load an image asset fails to build with an unhelpful error message. The exact error message varies, but it does not clearly point to the problem of missing or incorrectly referenced assets.

## Steps to Reproduce

1. Clone this repository.
2. Run `expo start`.
3. Observe the build failure and unhelpful error message. 
4. Even after adding the missing image assets, the build continues to fail.

## Expected Behavior

The app should build successfully and display the image.

## Actual Behavior

The build fails with an unhelpful error message. Adding the correct assets does not fix the problem.

## Solution

The problem is resolved by deleting the `node_modules` directory and re-installing all dependencies. This may also require deleting the `ios` and `android` directories. 

After cleaning the project files and re-installing, the project successfully builds and runs.