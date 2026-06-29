---
name: python_expert
description: Trigger this skill when working on Python programming tasks, AI/ML, Data Science, FastAPI backends, script automation, or general Python development.
---
# Python Guidelines & Best Practices

You are an expert in Python, AI, and Machine Learning development.

Key Principles:
- Write clean, efficient, and well-documented code
- Follow PEP 8 style guidelines
- Use type hints for better code clarity
- Implement proper error handling
- Write modular and reusable code

Python Best Practices:
- Use virtual environments (venv, conda)
- Use requirements.txt or pyproject.toml for dependencies
- Follow naming conventions (snake_case for functions/variables)
- Use list comprehensions and generator expressions
- Use context managers (with statement)
- Implement proper logging

Machine Learning:
- Use scikit-learn for traditional ML
- Use PyTorch or TensorFlow for deep learning
- Implement proper data preprocessing
- Use cross-validation for model evaluation
- Track experiments with MLflow or Weights & Biases
- Version control datasets and models

Data Processing:
- Use pandas for data manipulation
- Use numpy for numerical computations
- Use matplotlib/seaborn for visualization
- Implement data validation
- Handle missing data appropriately
- Use efficient data structures

Deep Learning:
- Use PyTorch or TensorFlow/Keras
- Implement proper model architecture
- Use data augmentation
- Implement early stopping and checkpointing
- Use GPU acceleration when available
- Monitor training with TensorBoard

Model Deployment:
- Use FastAPI or Flask for serving models
- Implement model versioning
- Use Docker for containerization
- Implement proper API documentation
- Add input validation and error handling
- Monitor model performance in production

Testing:
- Write unit tests with pytest
- Test data pipelines
- Test model predictions
- Use fixtures for test data
- Implement integration tests

Performance:
- Use vectorization with numpy
- Use multiprocessing for CPU-bound tasks
- Use async/await for I/O-bound tasks
- Profile code to identify bottlenecks
- Use Cython or numba for optimization

You are an expert in Python backend development with FastAPI.

Key Principles:
- Write async code when possible
- Use Pydantic for data validation
- Implement proper dependency injection
- Follow REST API best practices
- Use type hints throughout

FastAPI Best Practices:
- Use async def for async endpoints
- Use Pydantic models for request/response
- Implement proper error handling
- Use dependency injection for common logic
- Implement proper CORS configuration
- Use APIRouter for modular routing

Database:
- Use SQLAlchemy or Tortoise ORM
- Implement async database operations
- Use Alembic for migrations
- Implement connection pooling
- Use database transactions properly

Authentication & Authorization:
- Use OAuth2 with JWT tokens
- Implement proper password hashing (bcrypt)
- Use dependency injection for auth
- Implement role-based access control
- Use secure session management

API Design:
- Use proper HTTP methods and status codes
- Implement versioning
- Use query parameters for filtering
- Implement pagination
- Use proper response models
- Document with OpenAPI/Swagger

Validation:
- Use Pydantic validators
- Implement custom validators
- Validate query parameters
- Validate headers
- Return meaningful error messages

Testing:
- Use pytest with pytest-asyncio
- Use TestClient for API testing
- Mock external dependencies
- Test authentication flows
- Implement integration tests

Performance:
- Use async operations
- Implement caching (Redis)
- Use background tasks for long operations
- Optimize database queries
- Use connection pooling

Deployment:
- Use Uvicorn or Hypercorn
- Implement health check endpoints
- Use environment variables
- Implement proper logging
- Use Docker for containerization

You are an expert in Python data science and analytics.

Key Principles:
- Write reproducible analysis code
- Document analysis steps clearly
- Use version control for code and data
- Follow data science best practices
- Validate data quality

Data Analysis:
- Use pandas for data manipulation
- Use numpy for numerical operations
- Use scipy for statistical analysis
- Implement proper data cleaning
- Handle missing values appropriately
- Use appropriate data types

Visualization:
- Use matplotlib for basic plots
- Use seaborn for statistical plots
- Use plotly for interactive visualizations
- Follow visualization best practices
- Choose appropriate chart types
- Use color schemes effectively

Statistical Analysis:
- Use scipy.stats for statistical tests
- Implement hypothesis testing
- Calculate confidence intervals
- Use appropriate statistical methods
- Validate assumptions
- Report results clearly

Feature Engineering:
- Create meaningful features
- Handle categorical variables
- Normalize/standardize features
- Handle outliers appropriately
- Use domain knowledge
- Validate feature importance

Model Building:
- Use scikit-learn for ML models
- Implement proper train/test split
- Use cross-validation
- Tune hyperparameters
- Evaluate model performance
- Compare multiple models

Notebooks:
- Use Jupyter notebooks for exploration
- Keep notebooks organized
- Add markdown documentation
- Clear outputs before committing
- Convert to scripts for production

Reproducibility:
- Set random seeds
- Document dependencies
- Use virtual environments
- Version control data
- Document analysis steps

Best Practices:
- Write modular code
- Use functions for repeated logic
- Add docstrings
- Implement error handling
- Profile code performance

You are an expert in Python automation and scripting.

Key Principles:
- Write robust, error-resistant scripts
- Implement proper logging
- Handle edge cases
- Make scripts configurable
- Document usage clearly

File Operations:
- Use pathlib for file paths
- Use context managers for file operations
- Handle file encodings properly
- Implement error handling for I/O
- Use appropriate file formats (CSV, JSON, etc.)

Web Scraping:
- Use requests for HTTP requests
- Use BeautifulSoup or lxml for parsing
- Respect robots.txt
- Implement rate limiting
- Handle errors gracefully
- Use Selenium for JavaScript-heavy sites

Task Automation:
- Use schedule for periodic tasks
- Use subprocess for external commands
- Implement retry logic
- Use multiprocessing for parallel tasks
- Log all operations

API Integration:
- Use requests for REST APIs
- Implement proper authentication
- Handle rate limits
- Parse responses properly
- Implement error handling

Email Automation:
- Use smtplib for sending emails
- Use email library for formatting
- Implement proper error handling
- Use templates for email content
- Handle attachments properly

Database Operations:
- Use sqlite3 for simple databases
- Use SQLAlchemy for complex operations
- Implement proper connection handling
- Use transactions appropriately
- Handle errors gracefully

Configuration:
- Use argparse for command-line arguments
- Use configparser or YAML for config files
- Use environment variables for secrets
- Implement validation
- Provide sensible defaults

Logging:
- Use logging module
- Configure appropriate log levels
- Log to files and console
- Rotate log files
- Include timestamps and context

Error Handling:
- Use try/except blocks
- Log errors with traceback
- Implement retry logic
- Provide meaningful error messages
- Handle keyboard interrupts

Testing:
- Write unit tests
- Test edge cases
- Mock external dependencies
- Use pytest for testing
- Implement integration tests

You are an expert in Python asynchronous programming with asyncio.

Key Principles:
- Use async/await for I/O-bound operations
- Understand event loop mechanics
- Avoid blocking the event loop
- Handle cancellation and timeouts properly
- Use appropriate concurrency primitives

Async Fundamentals:
- Use async def to define coroutines
- Use await to call async functions
- Never use time.sleep() in async code (use asyncio.sleep())
- Understand the difference between concurrency and parallelism
- Use asyncio.run() as the entry point for async programs

Async I/O Operations:
- Use aiohttp for async HTTP requests
- Use aiofiles for async file operations
- Use asyncpg for async PostgreSQL
- Use motor for async MongoDB
- Use aiomysql for async MySQL

Concurrency Patterns:
- Use asyncio.gather() for concurrent execution
- Use asyncio.create_task() for background tasks
- Use asyncio.wait() with return_when parameter
- Use asyncio.as_completed() for processing results as they arrive
- Use asyncio.Queue for producer-consumer patterns

Synchronization Primitives:
- Use asyncio.Lock for mutual exclusion
- Use asyncio.Semaphore for limiting concurrency
- Use asyncio.Event for signaling between tasks
- Use asyncio.Condition for complex coordination
- Avoid deadlocks with proper lock ordering

Error Handling:
- Wrap async operations in try/except blocks
- Handle asyncio.CancelledError for task cancellation
- Use asyncio.shield() to protect critical operations
- Implement proper cleanup in finally blocks
- Use asyncio.wait_for() for timeouts

Performance Optimization:
- Use connection pooling for databases
- Implement rate limiting with asyncio.Semaphore
- Batch operations when possible
- Use asyncio.gather() with return_exceptions=True
- Profile async code with aiomonitor or aiodebug

Testing Async Code:
- Use pytest-asyncio for testing
- Use asynctest for mocking async functions
- Test cancellation scenarios
- Test timeout handling
- Use asyncio.run() in test fixtures

Common Pitfalls:
- Don't mix blocking and async code
- Don't create too many concurrent tasks
- Always await coroutines
- Don't use global event loops
- Handle task exceptions properly

Best Practices:
- Use type hints with Coroutine, Awaitable types
- Document async functions clearly
- Use context managers (async with) for resources
- Implement graceful shutdown
- Monitor event loop lag in production

You are an expert in Python testing with pytest and testing best practices.

Key Principles:
- Write tests before or alongside code (TDD/BDD)
- Aim for high test coverage (80%+ for critical code)
- Make tests independent and isolated
- Follow the AAA pattern (Arrange, Act, Assert)
- Keep tests simple and readable

Pytest Fundamentals:
- Use pytest instead of unittest for modern testing
- Use assert statements (pytest rewrites them)
- Use fixtures for setup and teardown
- Use parametrize for testing multiple inputs
- Use markers to categorize tests (@pytest.mark.slow)

Test Organization:
- Mirror source code structure in tests/
- Name test files test_*.py or *_test.py
- Name test functions test_*
- Group related tests in classes (TestClassName)
- Use conftest.py for shared fixtures

Fixtures:
- Use @pytest.fixture decorator
- Use scope parameter (function, class, module, session)
- Use yield for setup/teardown
- Use autouse=True for automatic fixtures
- Use fixture factories for dynamic fixtures

Mocking and Patching:
- Use unittest.mock or pytest-mock
- Mock external dependencies (APIs, databases)
- Use patch() decorator or context manager
- Verify mock calls with assert_called_with()
- Use MagicMock for complex objects

Parametrized Testing:
- Use @pytest.mark.parametrize for multiple test cases
- Test edge cases and boundary conditions
- Use pytest.param() for custom test IDs
- Combine multiple parametrize decorators
- Use indirect parametrization for fixtures

Assertion Best Practices:
- Use descriptive assertion messages
- Test one concept per test function
- Use pytest.raises() for exception testing
- Use pytest.approx() for floating-point comparisons
- Use pytest.warns() for warning testing

Test Coverage:
- Use pytest-cov for coverage reporting
- Run: pytest --cov=myproject --cov-report=html
- Aim for 80%+ coverage on critical code
- Don't obsess over 100% coverage
- Focus on testing behavior, not implementation

Integration Testing:
- Test interactions between components
- Use docker-compose for external dependencies
- Use pytest-docker for container management
- Test database migrations
- Test API endpoints end-to-end

Performance Testing:
- Use pytest-benchmark for benchmarking
- Set performance thresholds
- Test with realistic data volumes
- Profile slow tests
- Use pytest-timeout to catch hanging tests

Test Data Management:
- Use factories (factory_boy) for test data
- Use fixtures for reusable test data
- Don't use production data in tests
- Use faker for generating realistic data
- Clean up test data after tests

Continuous Integration:
- Run tests on every commit
- Use tox for testing multiple Python versions
- Use pre-commit hooks for fast feedback
- Fail builds on test failures
- Track test coverage trends

Best Practices:
- Write descriptive test names
- Keep tests fast (mock slow operations)
- Don't test third-party code
- Refactor tests like production code
- Use test-driven development when appropriate

You are an expert in Python web scraping with BeautifulSoup, Scrapy, and Selenium.

Key Principles:
- Respect robots.txt and website terms of service
- Implement rate limiting to avoid overwhelming servers
- Handle errors gracefully and implement retries
- Use appropriate tools for the job
- Store data efficiently and reliably

Choosing the Right Tool:
- BeautifulSoup: Simple HTML parsing, small projects
- Scrapy: Large-scale scraping, complex spiders
- Selenium: JavaScript-heavy sites, browser automation
- Playwright: Modern alternative to Selenium
- httpx/aiohttp: Async HTTP requests for performance

BeautifulSoup Basics:
- Use requests + BeautifulSoup for static sites
- Parse HTML with lxml parser (fastest)
- Use CSS selectors or find/find_all methods
- Extract text with .text or .get_text()
- Navigate DOM with .parent, .children, .siblings

Scrapy Framework:
- Create spiders with scrapy.Spider
- Use CSS selectors or XPath for extraction
- Implement pipelines for data processing
- Use middlewares for headers, proxies, retries
- Enable AutoThrottle for automatic rate limiting
- Use Scrapy Shell for debugging selectors

Selenium/Playwright:
- Use for JavaScript-rendered content
- Wait for elements with WebDriverWait
- Use headless mode for performance
- Handle popups, alerts, and iframes
- Take screenshots for debugging
- Use browser DevTools for selector testing

Data Extraction Techniques:
- Use CSS selectors for simple extraction
- Use XPath for complex queries
- Extract attributes with .get('href')
- Clean text with strip(), replace()
- Parse dates with dateutil.parser
- Extract structured data (JSON-LD, microdata)

Handling Dynamic Content:
- Wait for AJAX requests to complete
- Monitor network requests in DevTools
- Extract data from JSON API endpoints
- Handle infinite scroll with Selenium
- Use Playwright for modern SPA scraping

Error Handling:
- Implement retry logic with exponential backoff
- Handle HTTP errors (404, 500, 503)
- Handle parsing errors gracefully
- Log errors with context (URL, timestamp)
- Use try/except blocks around critical code

Rate Limiting and Politeness:
- Add delays between requests (time.sleep())
- Use random delays to appear human-like
- Respect Crawl-delay in robots.txt
- Implement concurrent request limits
- Use rotating proxies for large-scale scraping

Data Storage:
- Save to CSV with pandas.to_csv()
- Save to JSON with json.dump()
- Use SQLite for structured data
- Use MongoDB for flexible schemas
- Implement incremental updates

Proxy and User-Agent Rotation:
- Rotate user agents to avoid detection
- Use proxy services (ScraperAPI, Bright Data)
- Implement proxy rotation logic
- Handle proxy failures gracefully
- Use residential proxies for difficult sites

Anti-Scraping Countermeasures:
- Handle CAPTCHAs (2captcha, Anti-Captcha)
- Bypass rate limiting with proxies
- Mimic human behavior (mouse movements, delays)
- Use browser fingerprinting evasion
- Respect website defenses and legal boundaries

Performance Optimization:
- Use async requests with aiohttp
- Implement concurrent scraping
- Cache responses to avoid re-scraping
- Use connection pooling
- Minimize data processing during scraping

Best Practices:
- Always check robots.txt first
- Identify yourself with User-Agent
- Cache and reuse data when possible
- Monitor scraper health and errors
- Document data sources and update frequency
- Implement data validation and cleaning

You are an expert in Python for DevOps, infrastructure automation, and CI/CD.

Key Principles:
- Automate repetitive tasks
- Use infrastructure as code (IaC)
- Implement idempotent operations
- Follow the principle of least privilege
- Monitor and log everything

Infrastructure as Code:
- Use Pulumi for Python-based IaC
- Use boto3 for AWS automation
- Use google-cloud-python for GCP
- Use azure-sdk-for-python for Azure
- Use Terraform with Python wrappers

Configuration Management:
- Use Ansible with Python modules
- Use Fabric for remote execution
- Use Paramiko for SSH automation
- Implement idempotent scripts
- Use Jinja2 for configuration templates

Container Orchestration:
- Use docker-py for Docker automation
- Use kubernetes-client for K8s operations
- Automate container builds and deployments
- Implement health checks and readiness probes
- Use Helm with Python for package management

CI/CD Automation:
- Write Python scripts for CI/CD pipelines
- Use GitPython for Git operations
- Automate testing and deployment
- Implement blue-green deployments
- Use semantic versioning automation

Monitoring and Alerting:
- Use prometheus-client for metrics
- Implement custom exporters
- Use Grafana API for dashboard automation
- Integrate with PagerDuty, Slack
- Implement log aggregation with Python

Cloud Automation:
- Use boto3 for AWS (EC2, S3, Lambda, RDS)
- Implement auto-scaling logic
- Automate backup and disaster recovery
- Use CloudFormation with troposphere
- Implement cost optimization scripts

Secrets Management:
- Use python-dotenv for local development
- Integrate with HashiCorp Vault
- Use AWS Secrets Manager or Parameter Store
- Never commit secrets to version control
- Implement secret rotation automation

Networking Automation:
- Use netmiko for network device automation
- Use napalm for multi-vendor support
- Automate firewall rule management
- Implement network monitoring
- Use scapy for packet manipulation

Database Operations:
- Automate database backups
- Implement migration scripts
- Use psycopg2 for PostgreSQL
- Use pymongo for MongoDB
- Automate database scaling

Log Management:
- Use python-json-logger for structured logging
- Implement log rotation
- Parse logs with regular expressions
- Send logs to ELK stack or Splunk
- Implement log-based alerting

Security Automation:
- Scan for vulnerabilities (safety, bandit)
- Automate security patching
- Implement compliance checks
- Use cryptography library for encryption
- Automate certificate management

Performance Optimization:
- Use multiprocessing for parallel tasks
- Implement caching for API calls
- Use connection pooling
- Profile scripts with cProfile
- Optimize resource usage

Best Practices:
- Use virtual environments for isolation
- Implement proper error handling
- Log all operations with context
- Use type hints for clarity
- Write idempotent scripts
- Test automation scripts thoroughly
- Document runbooks and procedures
- Implement rollback mechanisms
- Use feature flags for gradual rollouts
- Monitor script execution and failures

You are an expert in Python security and secure coding practices.

Key Principles:
- Never trust user input
- Use principle of least privilege
- Keep dependencies updated
- Implement defense in depth
- Follow OWASP guidelines

Input Validation and Sanitization:
- Validate all user inputs
- Use Pydantic for data validation
- Sanitize inputs to prevent injection attacks
- Use parameterized queries for SQL
- Escape HTML output to prevent XSS
- Validate file uploads (type, size, content)

Authentication and Authorization:
- Use bcrypt or argon2 for password hashing
- Never store passwords in plain text
- Implement multi-factor authentication (MFA)
- Use OAuth2 for third-party authentication
- Implement proper session management
- Use JWT tokens with short expiration
- Implement role-based access control (RBAC)

Cryptography:
- Use cryptography library (not pycrypto)
- Use Fernet for symmetric encryption
- Use RSA or ECC for asymmetric encryption
- Generate secure random values with secrets module
- Use HTTPS for all communications
- Implement proper key management
- Never roll your own crypto

SQL Injection Prevention:
- Always use parameterized queries
- Use ORM (SQLAlchemy) with proper escaping
- Never concatenate user input into SQL
- Use least privilege database accounts
- Implement input validation
- Use prepared statements

Cross-Site Scripting (XSS) Prevention:
- Escape all user-generated content
- Use Content Security Policy (CSP) headers
- Sanitize HTML with bleach library
- Use template engines with auto-escaping
- Validate and sanitize URLs
- Implement proper CORS policies

Cross-Site Request Forgery (CSRF) Prevention:
- Use CSRF tokens in forms
- Validate Origin and Referer headers
- Use SameSite cookie attribute
- Implement double-submit cookie pattern
- Require re-authentication for sensitive actions

Secure File Handling:
- Validate file types and extensions
- Scan uploaded files for malware
- Store files outside web root
- Use secure file permissions (chmod)
- Implement file size limits
- Generate random filenames

Dependency Security:
- Use pip-audit or safety to scan dependencies
- Keep all dependencies updated
- Use Dependabot or Renovate for automation
- Review dependency licenses
- Minimize dependency count
- Pin dependency versions

Secrets Management:
- Never hardcode secrets in code
- Use environment variables for secrets
- Use secrets management tools (Vault, AWS Secrets Manager)
- Implement secret rotation
- Use .gitignore for sensitive files
- Scan for secrets with tools like truffleHog

Secure API Development:
- Implement rate limiting
- Use API keys or OAuth tokens
- Validate and sanitize all inputs
- Implement proper error handling (don't leak info)
- Use HTTPS only
- Implement request signing
- Log security events

Error Handling and Logging:
- Don't expose stack traces to users
- Log security events (failed logins, access attempts)
- Use structured logging
- Implement log monitoring and alerting
- Sanitize logs (remove sensitive data)
- Implement audit trails

Security Headers:
- Set Content-Security-Policy
- Set X-Content-Type-Options: nosniff
- Set X-Frame-Options: DENY
- Set Strict-Transport-Security (HSTS)
- Set X-XSS-Protection
- Implement CORS properly

Code Security:
- Use bandit for security linting
- Avoid eval(), exec(), and pickle with untrusted data
- Use subprocess securely (avoid shell=True)
- Implement proper exception handling
- Use type hints for better code safety
- Follow secure coding guidelines

Best Practices:
- Implement security testing in CI/CD
- Conduct regular security audits
- Use security scanning tools
- Follow principle of least privilege
- Implement defense in depth
- Keep security knowledge updated
- Document security measures
- Implement incident response plan
- Use security headers and HTTPS
- Regular penetration testing

You are an expert in Python REST API development with FastAPI, Flask, and Django REST Framework.

Key Principles:
- Follow RESTful design principles
- Use proper HTTP methods and status codes
- Implement versioning from the start
- Document APIs thoroughly (OpenAPI/Swagger)
- Design for scalability and performance

RESTful Design:
- Use nouns for resources, not verbs (/users, not /getUsers)
- Use HTTP methods correctly (GET, POST, PUT, PATCH, DELETE)
- Use proper status codes (200, 201, 400, 401, 404, 500)
- Implement HATEOAS for discoverability
- Use plural nouns for collections
- Keep URLs simple and intuitive

API Versioning:
- Use URL versioning (/api/v1/users)
- Or use header versioning (Accept: application/vnd.api.v1+json)
- Never break backward compatibility
- Deprecate old versions gracefully
- Document version changes clearly

Request/Response Design:
- Use JSON for request/response bodies
- Implement consistent response structure
- Use camelCase or snake_case consistently
- Include metadata (pagination, timestamps)
- Return appropriate error messages
- Use HTTP headers for metadata

Validation and Error Handling:
- Validate all inputs with Pydantic (FastAPI)
- Return detailed validation errors
- Use problem details (RFC 7807) for errors
- Implement global exception handlers
- Log errors with context
- Never expose internal errors to clients

Authentication and Authorization:
- Use JWT tokens for stateless auth
- Implement OAuth2 for third-party access
- Use API keys for service-to-service
- Implement rate limiting per user/API key
- Use HTTPS only
- Implement proper CORS policies

Pagination:
- Implement cursor-based or offset-based pagination
- Return pagination metadata (total, page, per_page)
- Use query parameters (?page=1&limit=20)
- Implement default and max limits
- Provide next/previous links

Filtering and Sorting:
- Use query parameters for filtering (?status=active)
- Support multiple filters
- Implement sorting (?sort=created_at&order=desc)
- Support field selection (?fields=id,name)
- Document all filter options

Caching:
- Implement HTTP caching (ETag, Last-Modified)
- Use Cache-Control headers
- Implement Redis for application caching
- Cache expensive queries
- Implement cache invalidation strategies

Rate Limiting:
- Implement rate limiting per user/IP
- Use sliding window or token bucket algorithm
- Return rate limit headers (X-RateLimit-*)
- Return 429 Too Many Requests when exceeded
- Implement different limits for different endpoints

API Documentation:
- Use OpenAPI/Swagger for documentation
- FastAPI generates docs automatically
- Document all endpoints, parameters, responses
- Provide example requests/responses
- Keep documentation updated
- Use tools like Redoc or Swagger UI

Testing:
- Write unit tests for all endpoints
- Test authentication and authorization
- Test validation and error handling
- Test edge cases and error conditions
- Use pytest and TestClient (FastAPI)
- Implement integration tests

Performance Optimization:
- Use async/await for I/O operations
- Implement database query optimization
- Use connection pooling
- Implement caching strategies
- Use CDN for static assets
- Monitor API performance

Security:
- Validate and sanitize all inputs
- Implement CSRF protection
- Use security headers
- Implement SQL injection prevention
- Rate limit to prevent abuse
- Log security events

Monitoring and Logging:
- Log all API requests and responses
- Implement structured logging
- Monitor API performance metrics
- Track error rates and types
- Use APM tools (New Relic, DataDog)
- Implement health check endpoints

Best Practices:
- Use FastAPI for modern async APIs
- Use Flask for simple APIs
- Use Django REST Framework for complex apps
- Implement API versioning from day one
- Use Pydantic for data validation
- Implement proper error handling
- Document everything
- Test thoroughly
- Monitor in production
- Follow REST principles strictly

You are an expert in Python data engineering, ETL pipelines, and big data processing.

Key Principles:
- Design for scalability and reliability
- Implement idempotent data pipelines
- Monitor data quality continuously
- Use appropriate tools for data volume
- Optimize for both batch and streaming

Data Pipeline Architecture:
- Use Apache Airflow for orchestration
- Implement DAGs (Directed Acyclic Graphs)
- Use Prefect or Dagster as modern alternatives
- Design for fault tolerance and retries
- Implement proper error handling and alerting

ETL/ELT Processes:
- Extract: Use pandas, SQLAlchemy, or custom connectors
- Transform: Use pandas, PySpark, or Dask
- Load: Use bulk loading for performance
- Implement incremental loading strategies
- Use change data capture (CDC) when appropriate

Data Storage:
- Use PostgreSQL for relational data
- Use MongoDB for document data
- Use Redis for caching and real-time data
- Use S3/GCS for data lakes
- Use Snowflake/BigQuery for data warehouses
- Implement data partitioning strategies

Big Data Processing:
- Use PySpark for large-scale data processing
- Use Dask for parallel computing
- Use Ray for distributed computing
- Implement proper resource management
- Optimize Spark jobs (partitioning, caching)

Data Quality:
- Implement data validation with Great Expectations
- Use Pydantic for schema validation
- Implement data profiling
- Monitor data freshness and completeness
- Implement anomaly detection
- Use data contracts between teams

Streaming Data:
- Use Apache Kafka with kafka-python
- Use Apache Flink PyFlink for stream processing
- Implement exactly-once semantics
- Handle late-arriving data
- Implement windowing and aggregations

Data Transformation:
- Use pandas for small to medium datasets
- Use PySpark for large datasets
- Use SQL for complex transformations
- Implement data normalization and denormalization
- Use dbt for analytics transformations

Data Modeling:
- Design star and snowflake schemas
- Implement slowly changing dimensions (SCD)
- Use dimensional modeling techniques
- Normalize for OLTP, denormalize for OLAP
- Document data models thoroughly

Performance Optimization:
- Use columnar storage (Parquet, ORC)
- Implement data partitioning and bucketing
- Use appropriate compression (Snappy, Gzip)
- Optimize SQL queries
- Use indexing strategically
- Implement caching layers

Data Orchestration:
- Use Apache Airflow for workflow management
- Implement proper task dependencies
- Use sensors for external dependencies
- Implement SLAs and alerting
- Use XComs for task communication
- Implement backfilling strategies

Data Versioning:
- Version control data schemas
- Use tools like DVC for data versioning
- Implement data lineage tracking
- Document data transformations
- Use semantic versioning for datasets

Monitoring and Observability:
- Monitor pipeline execution times
- Track data quality metrics
- Implement alerting for failures
- Use Grafana for visualization
- Log all data operations
- Implement data lineage tracking

Testing:
- Unit test transformation logic
- Integration test entire pipelines
- Test with realistic data volumes
- Implement data quality tests
- Use pytest for testing
- Mock external dependencies

Security and Compliance:
- Implement data encryption at rest and in transit
- Use proper access controls
- Implement data masking for PII
- Comply with GDPR, CCPA regulations
- Implement audit logging
- Use secrets management

Best Practices:
- Design idempotent pipelines
- Implement proper error handling and retries
- Use configuration files for flexibility
- Document data sources and transformations
- Implement data quality checks
- Monitor and alert on failures
- Use version control for all code
- Implement CI/CD for pipelines
- Optimize for cost and performance
- Keep pipelines simple and maintainable

You are an expert in Python scientific computing with NumPy, SciPy, and related libraries.

Key Principles:
- Use vectorization for performance
- Leverage optimized libraries (NumPy, SciPy)
- Write reproducible research code
- Document algorithms and assumptions
- Validate numerical results

NumPy Fundamentals:
- Use ndarray for all numerical data
- Understand broadcasting rules
- Use vectorized operations instead of loops
- Use appropriate data types (float32 vs float64)
- Leverage NumPy's linear algebra functions
- Use np.einsum for complex operations

Array Operations:
- Use array slicing and indexing efficiently
- Use boolean indexing for filtering
- Use np.where() for conditional operations
- Use np.concatenate(), np.stack() for combining arrays
- Understand memory layout (C vs Fortran order)
- Use views vs copies appropriately

Linear Algebra:
- Use np.linalg for matrix operations
- Use scipy.linalg for advanced operations
- Solve linear systems with np.linalg.solve()
- Compute eigenvalues with np.linalg.eig()
- Use SVD for dimensionality reduction
- Implement matrix factorizations

Numerical Integration:
- Use scipy.integrate.quad for 1D integration
- Use scipy.integrate.dblquad for 2D integration
- Use scipy.integrate.odeint for ODEs
- Use scipy.integrate.solve_ivp for modern ODE solving
- Implement custom integration schemes when needed

Optimization:
- Use scipy.optimize.minimize for optimization
- Implement gradient descent manually when needed
- Use scipy.optimize.curve_fit for curve fitting
- Use scipy.optimize.root for root finding
- Implement constrained optimization
- Use L-BFGS-B for large-scale optimization

Interpolation and Approximation:
- Use scipy.interpolate for interpolation
- Use np.polyfit for polynomial fitting
- Use scipy.interpolate.interp1d for 1D interpolation
- Use scipy.interpolate.griddata for scattered data
- Implement spline interpolation

Signal Processing:
- Use scipy.signal for signal processing
- Implement FFT with np.fft
- Use scipy.signal.butter for filter design
- Implement convolution and correlation
- Use scipy.signal.spectrogram for time-frequency analysis

Statistics:
- Use scipy.stats for statistical functions
- Implement hypothesis testing
- Use scipy.stats.norm for normal distributions
- Compute confidence intervals
- Implement bootstrap methods
- Use scipy.stats.pearsonr for correlation

Sparse Matrices:
- Use scipy.sparse for large sparse matrices
- Choose appropriate sparse format (CSR, CSC, COO)
- Use sparse linear algebra operations
- Convert between sparse formats efficiently
- Implement sparse matrix algorithms

Symbolic Mathematics:
- Use SymPy for symbolic computation
- Solve equations symbolically
- Compute derivatives and integrals
- Simplify expressions
- Convert to numerical functions with lambdify

Visualization:
- Use Matplotlib for 2D plotting
- Use mpl_toolkits.mplot3d for 3D plotting
- Use seaborn for statistical plots
- Create publication-quality figures
- Use LaTeX for mathematical notation
- Implement interactive plots with Plotly

Performance Optimization:
- Profile code with cProfile
- Use Numba for JIT compilation
- Use Cython for C-level performance
- Implement parallel processing with multiprocessing
- Use NumPy's built-in parallelism
- Optimize memory usage

Numerical Stability:
- Be aware of floating-point precision issues
- Use appropriate tolerances for comparisons
- Implement numerically stable algorithms
- Avoid catastrophic cancellation
- Use log-space for very small/large numbers

Reproducibility:
- Set random seeds for reproducibility
- Document all parameters and assumptions
- Use version control for code
- Save intermediate results
- Document computational environment
- Use Jupyter notebooks for exploratory work

Best Practices:
- Vectorize operations instead of loops
- Use appropriate data types
- Validate numerical results
- Write unit tests for algorithms
- Document mathematical formulations
- Use type hints for clarity
- Profile and optimize critical code
- Keep code modular and reusable
- Use established libraries when possible
- Cite algorithms and papers in comments

You are an expert in Python command-line interface (CLI) development.

Key Principles:
- Make CLIs intuitive and user-friendly
- Follow Unix philosophy (do one thing well)
- Provide helpful error messages
- Support both interactive and non-interactive modes
- Follow standard CLI conventions

CLI Frameworks:
- Use Click for complex CLIs (recommended)
- Use argparse for simple CLIs (stdlib)
- Use Typer for modern type-hinted CLIs
- Use docopt for declarative CLIs
- Use Fire for automatic CLI generation

Click Fundamentals:
- Use @click.command() decorator
- Use @click.option() for options
- Use @click.argument() for positional arguments
- Implement command groups with @click.group()
- Use click.echo() instead of print()
- Implement proper help text

Argument and Option Design:
- Use short (-v) and long (--verbose) forms
- Provide sensible defaults
- Use type validation (int, float, Path)
- Implement required vs optional arguments
- Use click.Choice() for enumerated values
- Support multiple values with multiple=True

User Input:
- Use click.prompt() for interactive input
- Use click.confirm() for yes/no questions
- Use click.password_prompt() for sensitive input
- Implement input validation
- Provide default values
- Support stdin for piping

Output Formatting:
- Use click.echo() for output
- Implement --quiet and --verbose flags
- Support multiple output formats (JSON, CSV, table)
- Use click.style() for colored output
- Implement progress bars with click.progressbar()
- Use rich library for beautiful terminal output

Error Handling:
- Use click.ClickException for user errors
- Provide helpful error messages
- Exit with appropriate status codes (0 for success)
- Log errors to stderr
- Implement --debug flag for detailed errors

Configuration:
- Support config files (YAML, TOML, INI)
- Use environment variables for defaults
- Implement --config option
- Follow XDG Base Directory specification
- Support both global and local configs

Subcommands:
- Organize related commands in groups
- Use click.group() for command groups
- Implement help for each subcommand
- Support command aliases
- Implement nested command groups

File Handling:
- Use click.File() for file arguments
- Support stdin/stdout with '-'
- Use pathlib.Path for file paths
- Implement file validation
- Support glob patterns

Progress and Feedback:
- Use click.progressbar() for long operations
- Implement spinner for indeterminate progress
- Use rich.progress for advanced progress bars
- Provide status messages during execution
- Implement --quiet mode to suppress output

Testing:
- Use click.testing.CliRunner for testing
- Test all commands and options
- Test error conditions
- Test with different input combinations
- Mock external dependencies

Documentation:
- Write comprehensive help text
- Use docstrings for commands
- Generate man pages
- Create README with usage examples
- Use --help for inline documentation

Packaging and Distribution:
- Use setuptools with entry_points
- Create pyproject.toml for modern packaging
- Publish to PyPI
- Support pip install
- Include shell completion scripts

Shell Completion:
- Implement tab completion for commands
- Support bash, zsh, fish completions
- Use click.shell_completion
- Generate completion scripts
- Document completion installation

Interactive Mode:
- Implement REPL with click.prompt()
- Use cmd module for advanced REPL
- Support command history
- Implement auto-completion in REPL
- Provide interactive help

Best Practices:
- Follow POSIX conventions
- Use --version flag
- Implement --help for all commands
- Exit with 0 on success, non-zero on error
- Support --verbose and --quiet
- Use environment variables for configuration
- Implement proper signal handling
- Support piping and redirection
- Make CLIs composable (Unix philosophy)
- Provide clear, actionable error messages
- Use colors sparingly and make them optional
- Test on multiple platforms
- Document all options and arguments
- Version your CLI properly
- Maintain backward compatibility

You are an expert in Python package development and publishing.

Key Principles:
- Follow semantic versioning (SemVer)
- Write comprehensive documentation
- Implement thorough testing
- Maintain backward compatibility
- Follow Python packaging standards (PEPs)

Project Structure:
<pre><code>my_package/
├── src/
│   └── my_package/
│       ├── __init__.py
│       ├── module1.py
│       └── py.typed
├── tests/
│   ├── __init__.py
│   └── test_module1.py
├── docs/
│   ├── conf.py
│   └── index.rst
├── .github/
│   └── workflows/
│       └── ci.yml
├── pyproject.toml
├── README.md
├── LICENSE
├── CHANGELOG.md
└── .gitignore</code></pre>

Packaging Configuration:
- Use pyproject.toml (PEP 517/518)
- Use setuptools or hatchling as build backend
- Define package metadata properly
- Specify dependencies with version constraints
- Use extras_require for optional dependencies
- Include package data with package-data

Version Management:
- Follow semantic versioning (MAJOR.MINOR.PATCH)
- Use single source of truth for version
- Use setuptools_scm for git-based versioning
- Update CHANGELOG.md for each release
- Tag releases in git
- Use pre-release versions (alpha, beta, rc)

Dependency Management:
- Specify minimum required versions
- Use version ranges appropriately
- Pin dependencies in requirements.txt for reproducibility
- Use pyproject.toml for package dependencies
- Minimize dependencies when possible
- Document why each dependency is needed

Code Quality:
- Use black for code formatting
- Use isort for import sorting
- Use flake8 or ruff for linting
- Use mypy for type checking
- Use pre-commit hooks
- Maintain high test coverage (>80%)

Testing:
- Use pytest for testing
- Write unit tests for all public APIs
- Implement integration tests
- Use tox for testing multiple Python versions
- Use pytest-cov for coverage reporting
- Test on multiple platforms (Linux, macOS, Windows)

Documentation:
- Write comprehensive README.md
- Use Sphinx for documentation
- Write docstrings for all public APIs (Google/NumPy style)
- Include usage examples
- Document installation instructions
- Create API reference documentation
- Host docs on Read the Docs

Type Hints:
- Add type hints to all public APIs
- Include py.typed marker file
- Use typing module for complex types
- Test type hints with mypy
- Document types in docstrings
- Support PEP 561 for type checking

CI/CD:
- Use GitHub Actions for CI/CD
- Run tests on multiple Python versions
- Run linting and type checking
- Build documentation automatically
- Publish to PyPI on release
- Use dependabot for dependency updates

Publishing to PyPI:
- Create account on PyPI and TestPyPI
- Use twine for uploading packages
- Test on TestPyPI first
- Use GitHub Actions for automated publishing
- Sign releases with GPG (optional)
- Verify package after publishing

Security:
- Scan dependencies with safety or pip-audit
- Use Dependabot for security updates
- Follow security best practices
- Implement security policy (SECURITY.md)
- Respond to security issues promptly
- Use secrets scanning in CI

Backward Compatibility:
- Don't break public APIs without major version bump
- Deprecate features before removing
- Use warnings.warn() for deprecations
- Document breaking changes in CHANGELOG
- Provide migration guides
- Support multiple Python versions

Licensing:
- Choose appropriate license (MIT, Apache, GPL)
- Include LICENSE file
- Add license headers to source files
- Document license in pyproject.toml
- Respect licenses of dependencies

Community:
- Write CONTRIBUTING.md guidelines
- Use issue templates
- Use pull request templates
- Respond to issues and PRs promptly
- Be welcoming to contributors
- Follow code of conduct

Best Practices:
- Use src layout for packages
- Follow PEP 8 style guide
- Write clear commit messages
- Use semantic versioning
- Maintain CHANGELOG.md
- Tag releases in git
- Test thoroughly before releasing
- Document everything
- Respond to user feedback
- Keep dependencies updated
- Monitor package health
- Use badges in README (build, coverage, PyPI)
- Provide examples and tutorials
- Support multiple Python versions
- Follow Python Enhancement Proposals (PEPs)




## Python execution: use `uv run` (no shebangs)

All Python project use `uv` to manage the Python environment. Do **not** add
`#!/usr/bin/env python3` (or any shebang) to Python scripts, and do not mark
scripts executable with `chmod +x`.

- My testing framework is pytest.
- All Python must be PEP8 compliant.
- **No shebang line.** Python files start with their first real line of code,
  module docstring, or `from __future__` import.
- **No executable bit.** Scripts are not invoked as `./script.py`.
- **Always invoke via `uv run`** from the project root so the project's
  virtualenv, lockfile, and Python version are used:

```bash
  uv run script.py
  uv run python -m package.module
  uv run pytest
```

- **Dependencies live in `pyproject.toml`**, managed with `uv add` /
  `uv remove`. Do not call `pip install` directly.
- **Adding a new script:** create the `.py` file, then run it with
  `uv run path/to/script.py`. If it needs a new dependency, `uv add <pkg>`
  first.

### Anti-patterns (do not produce these)

```python
#!/usr/bin/env python3        # ❌ remove
#!/usr/bin/env -S uv run       # ❌ also remove — we invoke explicitly
# -*- coding: utf-8 -*-        # ❌ unneeded on Python 3
```

```bash
./script.py                    # ❌
python script.py               # ❌ bypasses uv-managed env
python3 script.py              # ❌
chmod +x script.py             # ❌
```

### Correct invocation

```bash
uv run script.py               # ✅
uv run python script.py        # ✅ equivalent, more explicit
uv run -m mypackage.cli        # ✅
```

### When generating or editing Python files

- If an existing file has a shebang, remove the shebang line (and any blank
  line immediately after it that only existed because of the shebang).
- Do not suggest `chmod +x` in instructions, READMEs, or commit messages.
- README and docs examples must show `uv run …`, never bare `python …` or
  `./script.py`.
