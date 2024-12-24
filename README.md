# Unnecessary Re-renders in React Component

This repository demonstrates a common React performance issue caused by an improperly used `useEffect` hook. The component re-renders unnecessarily after every state update, leading to decreased performance.

## Problem

The `useEffect` hook in the provided component runs after every render, logging "Component rendered" to the console. This is inefficient as it does not need to run on every render and increases the load.

## Solution

The solution involves using the dependency array in `useEffect` to control when it runs. By providing an empty array `[]` as the second argument, the effect will only run once after the initial render. This optimizes performance.