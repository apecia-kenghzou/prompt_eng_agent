# CRITIQUE REPORT

**Prompt Version**: 1.0.0
**Agent Type**: software_development/frontend_developer
**Severity Level**: Critical
**Confidence**: High
**Date**: 2025-11-28

---

## CRITICAL WEAKNESSES

### Weakness 1: No Decision Framework for Technology Selection
- **Description**: The prompt lists "React.js, Vue.js, Angular" with priorities but provides NO guidance on when to choose which framework
- **Impact**: Agent will arbitrarily pick frameworks without considering project requirements, team expertise, or use case fit
- **Evidence**: "choose appropriate technologies from the above stack" - but HOW to choose is undefined
- **Risk Level**: High

### Weakness 2: Missing Error Handling Strategy
- **Description**: No mention of error boundaries, exception handling, error logging, or user feedback patterns
- **Impact**: Implementations will lack robust error handling, leading to poor user experience and difficult debugging
- **Evidence**: Entire prompt has zero mentions of "error", "exception", "fallback", or "recovery"
- **Risk Level**: High

### Weakness 3: State Management Selection Ambiguity
- **Description**: Lists "Redux, Zustand, Context API" without criteria for choosing between them
- **Impact**: Inconsistent architecture decisions across projects
- **Evidence**: "State Management (Redux, Zustand, Context API)" - no decision matrix
- **Risk Level**: High

### Weakness 4: Vague Performance Optimization
- **Description**: Says "Performance Optimization" but provides zero specific techniques
- **Impact**: Agent won't know HOW to optimize - code splitting, lazy loading, memoization, etc.
- **Evidence**: Single line mention with no actionable guidance
- **Risk Level**: High

## MAJOR CONCERNS

### Concern 1: No API Integration Guidance
- **Issue**: Missing data fetching strategies
- **Current State**: No mention of REST, GraphQL, fetch patterns, caching
- **Problem**: Frontend apps need API integration - this is a fundamental gap
- **Recommendation**: Add section on data fetching libraries (React Query, SWR, Axios) and patterns

### Concern 2: Insufficient Responsive Design Specifics
- **Issue**: Says "Responsive Design" but no breakpoint strategy
- **Current State**: "Responsive Design" as single bullet point
- **Problem**: No mobile-first approach, breakpoint system, or device testing requirements
- **Recommendation**: Specify breakpoint strategy (mobile 320-767px, tablet 768-1023px, desktop 1024px+)

### Concern 3: Testing Strategy Underspecified
- **Issue**: Lists tools but not testing methodology
- **Current State**: "Testing (Jest, React Testing Library)"
- **Problem**: Doesn't specify unit vs integration vs E2E, coverage targets per type, or testing pyramid
- **Recommendation**: Define testing levels and strategies for each

### Concern 4: No Browser Compatibility Requirements
- **Issue**: Missing minimum browser versions
- **Current State**: No browser requirements mentioned
- **Problem**: Agent won't know which browsers to support or test against
- **Recommendation**: Specify browser matrix (Chrome 90+, Firefox 88+, Safari 14+, Edge 90+)

### Concern 5: Accessibility Implementation Gap
- **Issue**: Demands 100% score but no implementation guidance
- **Current State**: "Accessibility Score 100%" as success metric
- **Problem**: No mention of ARIA labels, keyboard navigation, screen reader testing, focus management
- **Recommendation**: Add specific accessibility implementation requirements

## MINOR IMPROVEMENTS

- Add form validation libraries and patterns (React Hook Form, Formik)
- Specify image optimization requirements (WebP, lazy loading)
- Include performance monitoring tools (Web Vitals, Lighthouse CI)
- Add security best practices (XSS prevention, CSP headers)
- Mention code formatting standards (Prettier, ESLint configs)

## MISSING ELEMENTS

1. **Form Handling**: No mention of form libraries, validation patterns, or UX best practices
2. **Data Fetching**: Missing API integration strategies and libraries
3. **Routing**: No mention of client-side routing (React Router, Vue Router)
4. **Build Optimization**: Missing bundle size limits, tree shaking, code splitting strategies
5. **Development Workflow**: No Git workflow, code review standards, or deployment process
6. **Security Practices**: Beyond general mention - need specific XSS, CSRF, injection prevention
7. **Performance Monitoring**: How to track and measure metrics in production

## CONTRADICTIONS FOUND

- Demands "Lighthouse Score > 90" but allows "Page Load Time < 3s" (typically need < 2.5s for Lighthouse 90+)
- Requires "Accessibility Score 100%" but provides zero implementation guidance on HOW to achieve it

## EDGE CASES NOT COVERED

1. **Scenario**: Large dataset rendering (10,000+ items in a list)
   **Risk**: Performance degradation without virtualization (react-window, react-virtualized)

2. **Scenario**: Offline functionality for PWA
   **Risk**: PWA mentioned but no offline-first strategy, service worker patterns, or cache strategies defined

3. **Scenario**: Real-time data updates (WebSockets, SSE)
   **Risk**: No guidance on real-time communication patterns

4. **Scenario**: Internationalization (i18n)
   **Risk**: No mention of multi-language support, RTL layouts, locale handling

5. **Scenario**: Complex state synchronization across components
   **Risk**: No guidance on when to use global vs local state, state normalization

## ALTERNATIVE APPROACHES

### Option 1: Framework-Specific Prompts
Instead of one prompt covering React/Vue/Angular, create specialized prompts for each.
- **Pros**: More focused, deeper expertise per framework, clearer best practices
- **Cons**: More prompts to maintain, less flexibility

### Option 2: Example-Driven Approach
Include concrete code examples for common patterns
- **Pros**: Clearer expectations, reduces ambiguity, easier to understand
- **Cons**: May bias toward specific patterns, could become outdated

## BENCHMARK COMPARISON

- **Industry Standard**: Modern frontend prompts include API integration, error handling, and specific optimization techniques
- **Best Practice**: Decision frameworks for technology selection based on project scale, team size, and requirements
- **Missing**: This prompt is more of a technology checklist than an actionable guide

## SUMMARY

- **Critical Issues**: 4 (Decision frameworks, error handling, state management ambiguity, performance specifics)
- **Major Concerns**: 5 (API integration, responsive design, testing strategy, browser compatibility, accessibility)
- **Minor Improvements**: 5 (Forms, images, monitoring, security, formatting)
- **Overall Assessment**: Critical

**Recommendation**: This prompt requires significant enhancements before it can effectively guide development. Address all critical weaknesses immediately, particularly:
1. Add decision frameworks for technology selection
2. Define error handling strategies
3. Specify performance optimization techniques
4. Add API integration guidance
