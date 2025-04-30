## Beginner Level – Fundamentals & CLI

### 🔹 What is Angular?
- Angular is a TypeScript-based open-source front-end framework.
- Developed and maintained by Google.
- Component-based architecture.

### 🔸 Angular CLI Commands (Flashcards)
- `ng new app-name` – Create a new project
- `ng serve` – Run dev server
- `ng generate component name` – Create component
- `ng build` – Build the app
- `ng test` – Run unit tests

### 🔹 Core Concepts
- **Modules**: Grouping components/services (`AppModule`)
- **Components**: UI blocks (`@Component`)
- **Templates**: HTML + directives
- **Data Binding**: One-way, two-way (`[(ngModel)]`)
- **Directives**: `*ngIf`, `*ngFor`, `ngClass`, custom

### 🔸 Dependency Injection (DI)
- Angular provides built-in DI with `@Injectable()`
- Services are singleton by default in `providedIn: 'root'`

### 🔹 Forms
- Template-driven forms: easy, less code
- Reactive forms: scalable, testable

### 🔸 Routing Basics
- Set up with `RouterModule.forRoot()`
- Define routes in `app-routing.module.ts`
```ts
{ path: 'home', component: HomeComponent }
```

---

## Mid-Level – RxJS, State, HTTP, Testing

### 🔹 RxJS Observables
- Asynchronous streams (alternative to Promises)
- Operators: `map`, `switchMap`, `filter`, `debounceTime`
- Subscription lifecycle: unsubscribe on destroy

### 🔸 HTTP Client
- Use `HttpClientModule` to make REST API calls
- `http.get()`, `http.post()` return observables
- Interceptors for modifying requests/responses

### 🔹 Angular Routing (Advanced)
- Route Guards: `CanActivate`, `CanLoad`
- Lazy loading modules using `loadChildren`
- Route Resolvers for pre-fetching data

### 🔸 Component Interaction
- Input/Output: `@Input()`, `@Output()`
- ViewChild/ViewChildren for DOM access
- Services for shared state

### 🔹 State Management
- Angular signals (16+ feature) for reactive state
- NGRX/NGXS: Redux-style state containers

### 🔸 Angular Material
- UI component library
- Import modules like `MatButtonModule`, `MatCardModule`
- Responsive layout with FlexLayout

### 🔹 Unit & Integration Testing
- Jasmine + Karma test runner
- `TestBed` for creating test modules
- `fixture.detectChanges()` and spying services

---

## Advanced Level – Performance, SSR, Architecture

### 🔹 Signals (Angular 16+)
- New reactive primitive: `signal(value)`
- Automatically tracks dependencies
```ts
const count = signal(0);
const double = computed(() => count() * 2);
```

### 🔸 Standalone Components
- No need for NgModules
- Use `@Component({ standalone: true })`

### 🔹 Server-Side Rendering (Angular Universal)
- Improves performance and SEO
- `@angular/platform-server`

### 🔸 Route-Level Code Splitting
- Lazy loading using `loadComponent` (Angular 14+)
```ts
{
  path: 'about',
  loadComponent: () => import('./about.component').then(m => m.AboutComponent)
}
```

### 🔹 Custom Directives & Pipes
- Create with `@Directive()` and `@Pipe()`
- Use `ng generate directive` / `ng generate pipe`

### 🔸 Performance Optimization
- `ChangeDetectionStrategy.OnPush`
- Use trackBy in `*ngFor`
- Memoization and signals

### 🔹 Deployment & CI/CD
- Angular CLI build: `ng build --configuration production`
- Deploy to Firebase, Netlify, Vercel, etc.
- GitHub Actions for automated CI/CD

### 🔸 Micro Frontends (Advanced)
- Module Federation with Webpack 5
- Independent deployable frontend modules

---

Use this categorized Angular 16+ guide as a printable reference, flashcard source, or interactive mind map foundation.

Would you like a formatted PDF, flashcards, or visual cheat sheet next?

