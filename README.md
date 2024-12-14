# Next.js 15 Client-Side Counter Bug

This repository demonstrates a bug in a Next.js 15 application where a client-side counter implemented using `useEffect` and `setInterval` stops working after navigating away from and back to the page containing the counter. The issue is related to missing key props in the Link component.

## Bug Description

The `About` page contains a counter that increments every second.  However, after navigating to another page and then returning to the `About` page, the counter stops updating.  The component re-renders, but the `setInterval` is not restarted correctly.

## Solution

The solution involves adding a key prop to the Link component to force a re-render when navigating to the /about page.