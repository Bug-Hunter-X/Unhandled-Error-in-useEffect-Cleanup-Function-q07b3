# Unhandled Error in React Native useEffect Cleanup Function

This repository demonstrates a subtle bug in React Native where an error thrown within the cleanup function of a `useEffect` hook goes unhandled, leading to unexpected behavior or crashes. The error is difficult to track down because React Native's error reporting isn't always explicit in these cases.

## The Problem

The issue arises when the cleanup function attempts actions that are no longer valid after the component has unmounted, such as accessing a DOM element or a resource that has been released. This often happens in asynchronous operations.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install`.
3. Run the app on a simulator or device.
4. Observe the (lack of) error handling.