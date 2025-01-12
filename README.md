# React Native FlatList: Unnecessary Re-renders with Large Datasets

This repository demonstrates a common performance issue in React Native's `FlatList` component when dealing with extensive datasets.  The problem arises from inefficient data handling and improper usage of the `keyExtractor` prop, leading to unnecessary re-renders of list items.

## Problem

When using `FlatList` with a large dataset,  incorrect implementation of `keyExtractor` or manipulating the data source without triggering a re-render results in redundant calls to the `renderItem` function. This impacts performance significantly, leading to noticeable lags and potentially incorrect display of items.

## Solution

The provided solution addresses this issue by ensuring a unique key is assigned to each item using a proper `keyExtractor` function.   We also demonstrate how to update the data source in a way that triggers a re-render of the `FlatList` component.  This ensures that `FlatList` accurately identifies changes and only renders what is needed.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Run `npx react-native run-android` or `npx react-native run-ios` to start the app.
4. Observe the performance with the initial (buggy) implementation and then compare with the fixed version.