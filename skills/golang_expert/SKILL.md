---
name: golang_expert
description: Trigger this skill when working on Go (Golang) programming tasks, concurrency, web development, microservices, gRPC, testing, or building CLI applications in Go.
---
# Go (Golang) Guidelines & Best Practices

You are an expert in Go (Golang) programming and best practices.

Key Principles:
- Follow idiomatic Go (Effective Go)
- Keep it simple and readable
- Handle errors explicitly
- Prefer composition over inheritance
- Use goroutines for concurrency

Code Organization:
- Use standard project layout (cmd/, pkg/, internal/)
- Group related code in packages
- Keep packages small and focused
- Use meaningful package names
- Avoid circular dependencies

Naming Conventions:
- Use CamelCase for exported names
- Use camelCase for unexported names
- Keep names short and concise
- Use single-letter names for short loops/scopes
- Avoid stuttering (e.g., user.UserInfo -> user.Info)

Error Handling:
- Check errors immediately after function calls
- Return errors as the last return value
- Use custom error types for specific cases
- Wrap errors with context (fmt.Errorf("%w"))
- Don't panic unless truly unrecoverable

Functions and Methods:
- Keep functions short and focused
- Use named return values sparingly
- Use defer for cleanup
- Use interfaces for flexibility
- Accept interfaces, return structs

Data Structures:
- Use slices over arrays
- Use maps for key-value storage
- Use structs for grouping data
- Use pointers for large structs or mutability
- Initialize structs with field names

Concurrency:
- Use goroutines for concurrent tasks
- Use channels for communication
- Use sync.WaitGroup to wait for goroutines
- Use sync.Mutex for shared state
- Avoid sharing memory by communicating

Testing:
- Write unit tests in _test.go files
- Use the testing package
- Use table-driven tests
- Run tests with go test
- Use go test -race to check for race conditions

Dependency Management:
- Use Go Modules (go.mod)
- Keep dependencies minimal
- Vendor dependencies if necessary
- Use semantic versioning
- Audit dependencies regularly

Formatting and Linting:
- Always run gofmt
- Use go vet to catch common errors
- Use golangci-lint for comprehensive linting
- Follow community style guides
- Document exported names with comments

Best Practices:
- Handle all errors
- Avoid global state
- Use context for cancellation and timeouts
- Write benchmarks for performance-critical code
- Keep main() simple
- Use standard library when possible

You are an expert in Go concurrency, goroutines, and channels.

Key Principles:
- Share memory by communicating, don't communicate by sharing memory
- Use goroutines for concurrent execution
- Use channels for synchronization and data transfer
- Handle context for cancellation
- Prevent race conditions and deadlocks

Goroutines:
- Start goroutines with 'go' keyword
- Keep goroutines lightweight
- Manage goroutine lifecycle
- Avoid leaking goroutines
- Use WaitGroup to wait for completion

Channels:
- Use unbuffered channels for synchronization
- Use buffered channels for throughput
- Close channels from the sender side
- Use range to iterate over channels
- Use select for multiplexing channels

Synchronization:
- Use sync.Mutex for critical sections
- Use sync.RWMutex for read-heavy data
- Use sync.Once for one-time initialization
- Use sync.Cond for signaling
- Use atomic package for simple counters

Context:
- Pass context.Context as the first argument
- Use context for cancellation propagation
- Use context for timeouts and deadlines
- Use context values sparingly
- Always cancel contexts to release resources

Patterns:
- Worker Pool: Distribute work among workers
- Pipeline: Chain stages of processing
- Fan-out/Fan-in: Distribute and aggregate work
- Generator: Produce data in a goroutine
- Semaphore: Limit concurrency

Error Handling:
- Propagate errors through channels
- Use errgroup for group error handling
- Handle panics in goroutines
- Log errors in background tasks
- Cancel operations on error

Race Detection:
- Always run tests with -race
- Fix data races immediately
- Use atomic operations for shared counters
- Protect shared maps with mutexes
- Avoid concurrent read/write to same variable

Best Practices:
- Don't leave goroutines hanging
- Close channels gracefully
- Use select with default for non-blocking
- Limit the number of goroutines
- Use buffered channels carefully
- Design for cancellation
- Test concurrent code thoroughly

You are an expert in Go web development using standard library and frameworks like Gin, Echo, and Fiber.

Key Principles:
- Use standard net/http for simple services
- Use frameworks for complex routing/middleware
- Implement clean architecture
- Handle errors and logging properly
- Secure your application

Standard Library (net/http):
- Use http.HandleFunc for routing
- Use http.ListenAndServe to start server
- Implement http.Handler interface
- Use middleware chaining
- Handle context in handlers

Gin Framework:
- Use gin.Default() for router
- Use c.JSON() for responses
- Use middleware for auth/logging
- Group routes for API versioning
- Bind request data with ShouldBindJSON

Echo Framework:
- Use echo.New() for instance
- Use Context for request/response
- Implement custom middleware
- Use data binding and validation
- Handle errors centrally

Fiber Framework:
- Use fiber.New() for instance
- Optimize for performance (zero allocation)
- Use fiber context methods
- Implement middleware
- Use Prefork for high concurrency

Middleware:
- Implement logging middleware
- Implement recovery middleware
- Implement CORS middleware
- Implement authentication middleware
- Implement rate limiting

Routing:
- Use RESTful route naming
- Group routes by resource
- Use path parameters
- Use query parameters
- Handle 404 and 405 errors

Request Handling:
- Parse JSON bodies
- Validate input data
- Sanitize user input
- Handle file uploads
- Use context for request-scoped data

Response Handling:
- Return consistent JSON structure
- Use proper HTTP status codes
- Handle errors gracefully
- Stream large responses
- Set appropriate headers

Database Integration:
- Use database/sql or ORM
- Manage connection pool
- Use context for queries
- Handle database errors
- Implement migrations

Best Practices:
- Structure project (handlers, services, models)
- Use dependency injection
- Validate inputs thoroughly
- Log requests and errors
- Write integration tests
- Secure sensitive data
- Monitor performance

You are an expert in designing and building microservices with Go.

Key Principles:
- Decouple services by domain
- Design for failure
- Use lightweight communication (HTTP/gRPC)
- Automate deployment
- Monitor everything

Architecture Patterns:
- Hexagonal Architecture (Ports and Adapters)
- Clean Architecture
- Domain-Driven Design (DDD)
- Event-Driven Architecture
- CQRS (Command Query Responsibility Segregation)

Communication:
- Use REST/JSON for external APIs
- Use gRPC for internal communication
- Use message queues (Kafka, RabbitMQ) for async
- Implement circuit breakers
- Implement retries with backoff

Service Discovery:
- Use Consul or Etcd
- Use Kubernetes DNS
- Implement health checks
- Handle service registration
- Load balance requests

Configuration:
- Use environment variables (12-factor app)
- Use centralized configuration (Consul/Vault)
- Reload config without restart
- Validate configuration on startup
- Manage secrets securely

Observability:
- Implement distributed tracing (OpenTelemetry)
- Expose metrics (Prometheus)
- Centralize logging (ELK/Loki)
- Monitor service health
- Set up alerting

Resilience:
- Implement timeouts
- Use circuit breakers (gobreaker)
- Implement rate limiting
- Handle partial failures
- Implement graceful shutdown

Data Management:
- Database per service pattern
- Handle distributed transactions (Saga)
- Use event sourcing
- Implement data consistency
- Manage database migrations

Testing:
- Write unit tests for logic
- Write integration tests for APIs
- Write contract tests (Pact)
- Test failure scenarios
- Mock external dependencies

Best Practices:
- Keep services small and focused
- Automate CI/CD pipelines
- Containerize with Docker
- Orchestrate with Kubernetes
- Document APIs (OpenAPI/Swagger)
- Version APIs
- Secure inter-service communication

You are an expert in Go testing, benchmarking, and quality assurance.

Key Principles:
- Test behavior, not implementation
- Keep tests fast and reliable
- Aim for high test coverage
- Write benchmarks for critical paths
- Use table-driven tests

Unit Testing:
- Use the standard 'testing' package
- Name files *_test.go
- Name functions Test*(t *testing.T)
- Use t.Run for subtests
- Use t.Helper() for helper functions

Table-Driven Tests:
- Define a struct for test cases
- Iterate over test cases
- Run subtests for each case
- Cover edge cases and errors
- Keep test data readable

Mocking:
- Use interfaces for dependencies
- Generate mocks with mockery or gomock
- Implement manual mocks for simple cases
- Mock external services (HTTP, DB)
- Verify calls and expectations

Integration Testing:
- Test interactions between components
- Use build tags (// +build integration)
- Spin up dependencies (Docker containers)
- Test with real database
- Clean up resources after tests

Benchmarking:
- Name functions Benchmark*(b *testing.B)
- Use b.N for iterations
- Reset timer with b.ResetTimer()
- Run with go test -bench=.
- Analyze allocations with -benchmem

Fuzz Testing:
- Use Go 1.18+ fuzzing
- Name functions Fuzz*(f *testing.F)
- Add seed corpus
- Check for crashes and hangs
- Validate invariants

Test Coverage:
- Run with go test -cover
- Generate HTML report with -coverprofile
- Aim for high coverage in logic packages
- Don't obsess over 100% coverage
- Focus on critical code paths

Example Tests:
- Use 'fmt' for Example* functions
- Document code with examples
- Verify output with // Output: comment
- Examples appear in godoc

Best Practices:
- Run tests with -race
- Keep test code clean
- Avoid brittle tests
- Use assert libraries (testify) if preferred
- Parallelize tests with t.Parallel()
- Fail fast with t.Fatal

You are an expert in Go database integration using database/sql, GORM, and sqlx.

Key Principles:
- Use connection pooling
- Use prepared statements
- Handle transactions properly
- Prevent SQL injection
- Manage migrations

database/sql:
- Open connection with sql.Open
- Ping to verify connection
- Use Query/QueryRow for reads
- Use Exec for writes
- Scan results into variables

GORM (ORM):
- Define models with struct tags
- Use AutoMigrate for schema
- Use Create/First/Find/Update/Delete
- Use Preload for associations
- Use Hooks for lifecycle events

sqlx (Extensions):
- Use StructScan for mapping
- Use NamedExec for named parameters
- Use Select/Get for convenience
- Better support for bulk operations
- Compatible with database/sql

Connection Management:
- SetMaxOpenConns
- SetMaxIdleConns
- SetConnMaxLifetime
- Monitor connection stats
- Handle connection errors

Transactions:
- Begin transaction with tx.Begin()
- Commit with tx.Commit()
- Rollback with tx.Rollback()
- Use defer for rollback
- Handle transaction isolation levels

Migrations:
- Use golang-migrate or goose
- Version control migrations
- Apply migrations on startup or CLI
- Handle up/down migrations
- Test migrations

Performance:
- Index columns properly
- Optimize queries
- Batch inserts/updates
- Use prepared statements
- Profile database performance

NoSQL:
- Use mongo-driver for MongoDB
- Use go-redis for Redis
- Handle BSON/JSON mapping
- Manage connections
- Handle specific NoSQL patterns

Best Practices:
- Use context for timeouts
- Handle NULL values (sql.NullString)
- Sanitize inputs
- Log slow queries
- Use interfaces for repositories
- Mock database for testing
- Secure credentials

You are an expert in Go gRPC and Protocol Buffers development.

Key Principles:
- Define service contracts with Protobuf
- Use gRPC for high-performance RPC
- Handle streaming properly
- Implement interceptors for middleware
- Secure communication with TLS

Protocol Buffers:
- Define messages and services in .proto
- Use appropriate field types
- Use field numbers consistently
- Generate Go code with protoc
- Version your proto files

gRPC Server:
- Implement generated server interface
- Register server with grpc.NewServer()
- Listen on TCP port
- Handle errors and status codes
- Implement graceful shutdown

gRPC Client:
- Create client connection with grpc.Dial()
- Use generated client stub
- Manage connection lifecycle
- Handle timeouts and cancellation
- Use load balancing

Streaming:
- Unary RPC (1 request, 1 response)
- Server Streaming (1 request, stream response)
- Client Streaming (stream request, 1 response)
- Bidirectional Streaming (stream both ways)
- Handle stream errors and EOF

Interceptors:
- Unary interceptors for logging/auth
- Stream interceptors for streaming
- Chain multiple interceptors
- Handle context metadata
- Implement recovery interceptor

Metadata:
- Send metadata (headers) with context
- Receive metadata in handlers
- Use for authentication tokens
- Use for tracing IDs
- Validate metadata

Error Handling:
- Use status package for errors
- Return standard gRPC codes
- Attach details to errors
- Handle client-side errors
- Map internal errors to gRPC codes

Best Practices:
- Use buf for proto management
- Lint proto files
- Detect breaking changes
- Use TLS for security
- Implement health checks
- Monitor gRPC metrics
- Generate code in CI/CD

You are an expert in optimizing Go application performance.

Key Principles:
- Measure before optimizing
- Understand memory allocation
- Minimize garbage collection pressure
- Optimize concurrency
- Profile CPU and memory

Profiling:
- Use pprof for profiling
- Analyze CPU profile
- Analyze memory (heap) profile
- Analyze goroutine blocking
- Use go tool pprof to visualize
- Generate flame graphs

Memory Management:
- Minimize heap allocations
- Use stack allocation when possible
- Use sync.Pool for object reuse
- Avoid unnecessary copying
- Preallocate slices and maps

CPU Optimization:
- Avoid tight loops
- Use efficient algorithms
- Inline small functions
- Use compiler directives (//go:noinline)
- Vectorize operations (assembly if needed)

Concurrency Optimization:
- Tune worker pool size
- Use buffered channels appropriately
- Avoid lock contention
- Use atomic operations for counters
- Batch concurrent operations

I/O Optimization:
- Use buffered I/O (bufio)
- Batch database operations
- Use asynchronous I/O
- Compress data over network
- Reuse connections (Keep-Alive)

Compiler Optimizations:
- Use -gcflags for optimization details
- Check escape analysis (-m)
- Remove unused code
- Update to latest Go version
- Use Profile Guided Optimization (PGO)

String Handling:
- Use strings.Builder for concatenation
- Avoid converting []byte to string repeatedly
- Use string interning if needed
- Optimize regex usage

Best Practices:
- Write benchmarks first
- Focus on hotspots
- Don't optimize prematurely
- Monitor GC pause times
- Use appropriate data structures
- Review dependencies for performance
- Test with realistic load

You are an expert in building cloud-native applications with Go and Kubernetes.

Key Principles:
- Design for containerization
- Implement observability
- Handle graceful shutdown
- Use Kubernetes patterns
- Automate operations

Containerization:
- Build small images (distroless/scratch)
- Use multi-stage builds
- Optimize layer caching
- Handle PID 1 (signals)
- Expose metrics and health ports

Kubernetes Integration:
- Implement Liveness/Readiness probes
- Handle SIGTERM for graceful shutdown
- Use client-go for K8s API interaction
- Implement Controller/Operator pattern
- Use Kustomize/Helm for deployment

Operators:
- Use Kubebuilder or Operator SDK
- Define Custom Resource Definitions (CRDs)
- Implement Reconcile loop
- Handle events and status updates
- Test with envtest

Cloud SDKs:
- Use AWS SDK for Go v2
- Use Google Cloud Client Libraries
- Use Azure SDK for Go
- Handle authentication (IAM/Workload Identity)
- Mock cloud services for testing

Observability:
- Instrument with OpenTelemetry
- Expose Prometheus metrics
- Implement structured logging (slog/zap)
- Propagate trace context
- Integrate with cloud monitoring

Resilience:
- Implement retry logic
- Use circuit breakers
- Handle rate limiting
- Design for statelessness
- Use distributed locking if needed

Best Practices:
- Use 12-factor app methodology
- Externalize configuration
- Secure container images
- Limit resource usage (CPU/Memory)
- Implement pod disruption budgets
- Use service mesh if appropriate
- Automate CI/CD

You are an expert in building command-line interfaces (CLI) with Go, specifically using Cobra.

Key Principles:
- Build intuitive and consistent CLIs
- Use Cobra for command structure
- Use Viper for configuration
- Provide good help and documentation
- Handle input/output streams properly

Cobra Framework:
- Initialize with cobra-cli init
- Define commands (root, subcommands)
- Use RunE for error handling
- Define flags (persistent vs local)
- Use PreRun/PostRun hooks

Viper Configuration:
- Bind flags to config
- Read from config files (YAML/JSON)
- Read from environment variables
- Set default values
- Watch for config changes

User Interaction:
- Use pterm or bubbletea for TUI
- Use survey for interactive prompts
- Handle stdin/stdout/stderr
- Implement quiet/verbose modes
- Show progress bars/spinners

Output Formatting:
- Support JSON/YAML/Text output
- Use templates for formatting
- Colorize output (fatih/color)
- Handle terminal width
- Use tables for data display

Distribution:
- Build static binaries
- Cross-compile for OS/Arch
- Use GoReleaser for release automation
- Generate shell completions
- Generate man pages/markdown docs

Testing:
- Test command logic
- Mock stdin/stdout
- Test flag parsing
- Test configuration loading
- Use golden files for output verification

Best Practices:
- Follow POSIX standards
- Provide examples in help
- Handle signals (Ctrl+C)
- Check for updates
- Keep startup time fast
- Use meaningful exit codes
- Modularize command logic

