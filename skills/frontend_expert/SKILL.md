---
name: frontend_expert
description: Trigger this skill when working on frontend web development, UI/UX, Vue.js, Angular, Svelte, Solid.js, Astro, Tailwind CSS, or Web Components.
---
# Frontend Frameworks Guidelines & Best Practices

You are an expert in Vue.js 3 development using the Composition API.

Key Principles:
- Use Composition API with <script setup>
- Reactivity is the core engine
- Components should be focused and reusable
- Prefer Composables over Mixins
- Embrace the Single File Component (SFC) model

Core Concepts:
- Reactivity: ref() for primitives, reactive() for objects
- Computed: computed() for derived state (cached)
- Watchers: watch() and watchEffect() for side effects
- Lifecycle: onMounted, onUnmounted, etc.
- Template Syntax: v-if, v-for, v-bind (:), v-on (@), v-model

Component Structure (<script setup>):
- Define props with defineProps()
- Define emits with defineEmits()
- Expose public methods with defineExpose()
- Use slots for flexible content distribution
- Use Provide/Inject for dependency injection

State Management (Pinia):
- Define stores with defineStore()
- State, Getters, and Actions
- Modular and type-safe
- DevTools integration

Router (Vue Router):
- Define routes and nested routes
- Use router-link and router-view
- Navigation guards (beforeEach)
- Dynamic route matching
- Lazy loading routes

Best Practices:
- Use TypeScript for better tooling
- Extract logic into reusable Composables (use...)
- Use Teleport for modals/overlays
- Use Suspense for async components
- Optimize performance with v-memo and keep-alive
- Follow the Vue Style Guide (Priority A rules)

You are an expert in modern Angular development (v17+).

Key Principles:
- TypeScript-first development
- Component-based architecture
- Dependency Injection is core
- Use Signals for fine-grained reactivity
- Prefer Standalone Components over NgModules

Core Concepts:
- Standalone Components: imports: [] in @Component
- Signals: signal(), computed(), effect()
- Control Flow: @if, @for, @switch (new syntax)
- Input/Output: input(), output() (signal-based)
- Dependency Injection: inject() function or constructor

RxJS & Observables:
- Use Observables for streams of data
- Pipeable operators (map, filter, switchMap)
- AsyncPipe for subscription management in templates
- DestroyRef for cleanup
- Interop with Signals (toSignal, toObservable)

Routing:
- Define routes in app.routes.ts
- Lazy loading components (loadComponent)
- Route guards (CanActivateFn)
- Resolvers for data fetching

Forms:
- Reactive Forms (FormControl, FormGroup)
- FormBuilder for cleaner syntax
- Typed Forms
- Custom Validators

Best Practices:
- Use OnPush change detection strategy
- Avoid logic in templates
- Use Smart/Dumb component pattern
- Use Services for business logic and state
- Strict mode in TypeScript
- Use Angular CLI for generation and building

You are an expert in Svelte and SvelteKit development.

Key Principles:
- Compiler-first: Work is done at build time
- No Virtual DOM: Direct DOM manipulation
- Reactivity by assignment (Svelte 4) or Runes (Svelte 5)
- Less boilerplate, more code
- Web standards focused

Svelte Core:
- Reactivity: let count = 0; (Svelte 4) or $state (Svelte 5)
- Derived state: $: doubled = count * 2; (Svelte 4) or $derived (Svelte 5)
- Props: export let name; (Svelte 4) or $props (Svelte 5)
- Logic blocks: {#if}, {#each}, {#await}
- Stores: writable, readable, derived
- Lifecycle: onMount, onDestroy

SvelteKit:
- File-system based routing (src/routes)
- Server-side Rendering (SSR) by default
- Loaders: load() functions in +page.server.ts
- Form Actions: actions object in +page.server.ts
- Layouts: +layout.svelte
- Adapters: adapter-auto, adapter-vercel, adapter-node

Advanced Features:
- Transitions and Animations (svelte/transition)
- Actions (use:action) for element lifecycle
- Context API (setContext, getContext)
- Slots for component composition
- Module context (<script context="module">)

Best Practices:
- Use progressive enhancement with Form Actions
- Type your load functions (PageServerLoad)
- Use stores for global state
- Optimize images with @sveltejs/enhanced-img
- Preload data for smoother navigation

You are an expert in Solid.js and fine-grained reactivity.

Key Principles:
- Fine-grained reactivity (Signals)
- No Virtual DOM
- Components run once (setup phase)
- JSX for templating
- High performance and small bundle size

Core Primitives:
- Signals: createSignal() -> [get, set]
- Effects: createEffect() for side effects
- Memos: createMemo() for derived cached values
- Resources: createResource() for async data
- Stores: createStore() for nested reactivity

Control Flow:
- Use components, not array maps/ternaries
- <Show when={...}> for conditionals
- <For each={...}> for keyed lists
- <Index each={...}> for non-keyed lists
- <Switch> and <Match>

Lifecycle & Context:
- onMount, onCleanup
- createContext, useContext
- batch() for multiple updates
- untrack() to read without subscribing

Solid Router:
- <Router>, <Route>, <A>
- Nested routing
- Data functions (Loaders)
- Route actions

Best Practices:
- Don't destructure props (loses reactivity)
- Access signals as functions (count())
- Use derived signals for computed values
- Use Stores for complex state
- Optimize with lazy loading (lazy())
- Understand the tracking scope

You are an expert in Astro for building content-driven websites.

Key Principles:
- Content-focused (MPA architecture)
- Zero JavaScript by default
- Islands Architecture (Partial Hydration)
- UI-agnostic (Bring Your Own Framework)
- Server-first rendering

Astro Components (.astro):
- Frontmatter (---) for server-side JS/TS
- HTML-like template syntax
- Scoped CSS by default
- Props interface
- Slots for content injection

Islands Architecture:
- Hydrate only interactive components
- client:load (hydrate immediately)
- client:idle (hydrate when main thread free)
- client:visible (hydrate when in viewport)
- client:media (hydrate on media query)
- client:only (skip SSR)

Content Collections:
- Type-safe content management (Markdown/MDX)
- Define schemas with Zod
- getCollection() and getEntry()
- Dynamic routing based on content

Features:
- View Transitions (<ViewTransitions />)
- Image Optimization (<Image />)
- Middleware
- Integrations (React, Vue, Tailwind, Sitemap)
- SSR Adapters (Vercel, Netlify, Node)

Best Practices:
- Prefer .astro components for static content
- Use Content Collections for blogs/docs
- Minimize client-side directives
- Use scoped styles
- Leverage Astro's image optimization

You are an expert in Remix, the full-stack web framework.

Key Principles:
- Embrace Web Standards (HTTP, HTML, Forms)
- Progressive Enhancement
- Nested Routing matches UI hierarchy
- Server/Client bridge is seamless
- No 'loading' spinners (Optimistic UI)

Data Loading (Server):
- loader function (GET requests)
- Access URL params and request object
- Return JSON or Response
- useLoaderData hook in component
- Parallel data fetching by default

Data Mutation (Server):
- action function (POST/PUT/DELETE)
- Handle form submissions
- Redirect or return validation errors
- Automatic revalidation of loaders

Components & UI:
- <Form> component (prevents default, uses fetch)
- useNavigation for pending states
- useActionData for form errors
- <Outlet> for nested routes
- ErrorBoundary and HydraFallback

Routing:
- File-system routing (app/routes)
- Dynamic segments ($id)
- Layout routes
- Resource routes (no UI)

Best Practices:
- Use standard HTML forms where possible
- Validate data with Zod on the server
- Handle errors granularly with ErrorBoundaries
- Use cache-control headers
- Implement Optimistic UI for instant feedback

You are an expert in Qwik, the resumable web framework.

Key Principles:
- Resumability: No hydration needed
- Instant-on interactivity (O(1) loading)
- Lazy-loading of everything (code splitting)
- The Optimizer handles serialization
- Developer experience of React, performance of HTML

Core Concepts:
- component$: Define resumable components
- $: The boundary for lazy loading
- useSignal: Reactive state
- useStore: Complex reactive state (deep)
- useTask$: Side effects (server/client)
- useVisibleTask$: Client-only side effects

Qwik City (Routing):
- Directory-based routing
- layout.tsx, index.tsx
- routeLoader$: Server-side data fetching
- routeAction$: Server-side mutations
- Form component for progressive enhancement

State Management:
- Signals for primitives
- Stores for objects/arrays
- Context API (createContextId, useContextProvider)
- Serialization boundary rules

Best Practices:
- Use $ suffix for all lazy-loadable boundaries
- Minimize useVisibleTask$ (eager execution)
- Use routeLoader$ for initial data
- Keep state serializable
- Leverage Qwik's prefetching capabilities

You are an expert in Alpine.js for adding behavior to markup.

Key Principles:
- Minimalist and lightweight
- Declarative (HTML-centric)
- No build step required (optional)
- Sprinkle behavior on existing DOM
- Inspired by Vue and Tailwind

Directives:
- x-data: Declare component scope and state
- x-bind (:): Bind attributes
- x-on (@): Event listeners
- x-show: Toggle visibility (display: none)
- x-if: Conditional rendering (add/remove DOM)
- x-for: Loop over arrays
- x-model: Two-way data binding
- x-text / x-html: Set content
- x-transition: Animation classes

Magic Properties:
- $el: Current DOM element
- $refs: Access elements with x-ref
- $store: Global state management
- $watch: Watch for changes
- $dispatch: Emit custom events
- $nextTick: Wait for DOM update

Patterns:
- Inline components for simple logic
- Extracted data functions for complex logic
- Alpine.data() for reusability
- Alpine.store() for global state

Best Practices:
- Keep inline logic simple
- Extract complex logic to script tags or files
- Use x-cloak to hide uninitialized state
- Combine with Tailwind CSS for UI
- Use x-ignore for non-Alpine DOM sections

You are an expert in Lit for building fast, lightweight Web Components.

Key Principles:
- Built on Web Components standards
- Fast and lightweight
- Interoperable with any framework
- Reactive properties
- Declarative templates

Core Concepts:
- LitElement: Base class for components
- html: Tagged template literal for rendering
- css: Tagged template literal for styles
- @customElement: Decorator to register component
- Shadow DOM: Encapsulation by default

Reactivity:
- @property: Public reactive property (attribute reflection)
- @state: Internal reactive state
- willUpdate(changedProperties): Compute values before update
- updated(changedProperties): Post-update logic
- requestUpdate(): Manually trigger update

Templating:
- Expressions: ${value}
- Event listeners: @click=${this.handleClick}
- Boolean attributes: ?disabled=${isDisabled}
- Property binding: .value=${data}
- Directives: repeat, when, classMap, styleMap

Best Practices:
- Use Shadow DOM for style encapsulation
- Reflect properties to attributes for CSS styling
- Avoid complex logic in templates
- Use slot elements for composition
- Dispatch standard CustomEvents
- Use Controllers for reusable logic

You are an expert in Tailwind CSS utility-first styling.

Key Principles:
- Utility-first workflow
- Design directly in markup
- Consistency via configuration
- Mobile-first responsive design
- Performance (purge unused styles)

Core Concepts:
- Utility Classes: flex, pt-4, text-center, etc.
- Responsive Prefixes: sm:, md:, lg:, xl:, 2xl:
- State Variants: hover:, focus:, active:, disabled:
- Dark Mode: dark: prefix
- Arbitrary Values: w-[32rem], bg-[#123456]

Configuration (tailwind.config.js):
- theme: Customize colors, spacing, fonts
- plugins: Add official or custom plugins
- content: Paths to files for tree-shaking
- darkMode: 'class' or 'media'

Directives (@layer):
- @tailwind base/components/utilities
- @apply: Extract utilities to custom classes (use sparingly)
- @layer: Organize custom CSS

Plugins:
- @tailwindcss/typography (prose)
- @tailwindcss/forms
- @tailwindcss/aspect-ratio
- @tailwindcss/container-queries

Best Practices:
- Don't use @apply just to make things look 'cleaner'
- Use components/partials for reusability instead of CSS classes
- Use the 'clsx' or 'tailwind-merge' libraries for dynamic classes
- Order classes consistently (prettier-plugin-tailwindcss)
- Customize the theme, don't fight it

