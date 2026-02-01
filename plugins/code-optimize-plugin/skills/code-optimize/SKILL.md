---
description: Analyze and optimize code for performance, memory, and efficiency
model: claude-sonnet-4-5
---

Optimize the following code for performance and efficiency.

## Code to Optimize

$ARGUMENTS

## Optimization Strategy for Solo Developers

### 1. **Profiling First**
- Identify actual bottlenecks
- Don't optimize prematurely
- Measure before and after
- Focus on high-impact areas

### 2. **Performance Optimization Areas**

**Database Queries**
- Add indexes for frequently queried fields
- Batch queries (reduce N+1 problems)
- Use select to limit fields
- Implement pagination
- Cache frequent queries
- Use database views for complex joins

**API Calls**
- Implement caching (SWR, React Query)
- Debounce/throttle requests
- Parallel requests where possible
- Request deduplication
- Optimistic updates

**Bundle Size**
- Tree-shaking unused code
- Dynamic imports for large libraries
- Replace heavy dependencies
- Code splitting by route
- Lazy load below-the-fold content

**Memory**
- Fix memory leaks (cleanup useEffect)
- Avoid unnecessary object creation
- Use const for non-changing values
- Clear intervals/timeouts
- Remove event listeners

### 3. **Optimization Checklist**

**JavaScript/TypeScript**
-  Use const/let instead of var
-  Avoid nested loops where possible
-  Use Map/Set for lookups
-  Minimize DOM manipulations
-  Debounce/throttle expensive operations

**Database**
-  Add indexes on foreign keys
-  Use prepared statements
-  Batch inserts/updates
-  Implement connection pooling
-  Cache expensive queries

**Network**
-  Compress responses (gzip/brotli)
-  Use CDN for static assets
-  Implement HTTP/2
-  Set proper cache headers
-  Minimize payload size

### 4. **Measurement Tools**

**Frontend**
- Chrome DevTools Performance tab
- Lighthouse CI
- React DevTools Profiler
- Bundle Analyzer (next/bundle-analyzer)

**Backend**
- Node.js profiler
- Database query analyzer
- APM tools (DataDog, New Relic)
- Load testing (k6, Artillery)

### 5. **Common Optimizations**

**Replace inefficient array methods**
```typescript
// Before: Multiple iterations
const result = arr
  .filter(x => x > 0)
  .map(x => x * 2)
  .reduce((sum, x) => sum + x, 0)

// After: Single iteration
const result = arr.reduce((sum, x) => {
  return x > 0 ? sum + (x * 2) : sum
}, 0)
```

## Output Format

1. **Analysis** - Identify performance bottlenecks
2. **Optimized Code** - Improved version
3. **Explanation** - What changed and why
4. **Benchmarks** - Expected performance improvement
5. **Trade-offs** - Any complexity added
6. **Next Steps** - Further optimization opportunities

Focus on practical, measurable optimizations that provide real user value. Don't sacrifice readability for micro-optimizations.
