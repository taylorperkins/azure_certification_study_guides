# Describe the benefits and usage of Internet of Things (IoT) Hub, IoT Central, and Azure Sphere

When working with:
- Environmental sensors that capture temperature and humidity levels.
- Barcode, QR code, or optical character recognition (OCR) scanners.
- Geo-location and proximity sensors.
- Light, color, and infrared sensors.
- Sound and ultrasonic sensors.
- Motion and touch sensors.
- Accelerometer and tilt sensors.
- Smoke, gas, and alcohol sensors.
- Error sensors to detect when there's a problem with the device.
- Mechanical sensors that detect anomalies or deformations.
- Flow, level, and pressure sensors for measuring gasses and liquids.


## IoT Hub

- Central message hub for bi-directional communication between the IoT device and the manager
- Supports device-to-cloud telementry, file uploads from devices, and request-reply methods to control devices from the cloud
- Allows command and control (manual or automated remote control of all connected devices)


## IoT Central

- Builds on top of IoT Hub by adding in a dashboard that allows you to connect, monitor, and manage IoT devices
- Provides starter templates to help get up and running
- Device templates


## Azure Sphere

- End to end, highly securable IoT solution for customers
- 3 parts:
	- Sphere micro controller unit responsible for processing the OS and signals from attached sensors
	- Customized linux software system to handle communication with security devices
	- security service to ensure that the device has not been maliciously compromised


# Describe the benefits and usage of Azure Synapse Analytics, HDInsight, and Azure Databricks

## Azure Synapse

- unified experience to ingest, prepare, manage, and serve data for immediate BI and machine learning needs
- Limitless analytics service
- Enterprise data warehousing and big data analytics
- Serverless or provisioned resources
- Ingest, manage, serve data for immediate BI


## Databricks

- AI solutions
- Apache spark environment
- Python, scala, R, java, and SQL
- DS frameworks like tensorflow, PyTorch, and scikit-learn


## HDInsight

- Analytics service for enterprises
- Process massive amounts of data
- can run popular open-source frameworks and create cluster types such as Apache Spark , Apache Hadoop , Apache Kafka , Apache HBase , Apache Storm , and Machine Learning Services . 
- Run cluster types like spark, hadoop, kafka, HBase, Storm, and ML services
- Good for ETL


## Data Lakes Analytics

- Simplifies big data
- Write queries to transform data and extract valuable insights
- Pay as you go (jobs when running)


# Describe the benefits and usage of Azure Machine Learning, Cognitive Services and Azure Bot Service

- Deep Learning: Based on NN, learn through experience
- Machine Learning: Uses existing data to train the model, test, then apply
Machine Learning

- platform for making predictions
- Connect to data, train and test
- Train and evaluate predictive models
- create pipelines to define when / where to run compute experiments
- Deploy best - performing algorithm
- Predict future outcomes based on private historical data
- DIY model using your own data, or just something different than cognitive or bot


## Cognitive Services

- Enables apps to hear, see, speak, understand, and begin to reason
- 4 primary categories
	- Language
	- Speech
	- Vision
	- Decision
- understand content and meaning of images, video, or audio, or translating text to different languages
- predict user behavior to provide recommendations for your app


## Bot Service

- Creating virtual agents to understand and reply like humans (chat bot)
- Use cases include dinner reservations, gathering profile info etc
- Interfacing with humans via natural language


### Questions to ask when choosing a service

- Is the company building a virtual agent to interface with humans?
	- If yes, then Bot Service
- Does the company need to understand the content of video, meaning of images, audio, or translate text?
	- If yes, then Cognitive Services
- Does the company need to predict user behavior for personalized recommendations?
	- If yes, then Cognitive Services Personalizer
- Will the company need to predict future outcomes based on historical data?
	- If yes, then Machine Learning


# Describe the benefits and usage of serverless computing solutions that include Azure Functions and Logic Apps

## Functions

- Only care about the code, not the infrastructure or platform
- Good for responding to events, timers, or messages from other services
- Abstracts servers, infrastructure, and OS
- Scaling and performance is handled automatically
- Micro-billing
- Event-driven scale:
	- Timers (such as Cron)
	- HTTP API webhook scenarios
	- Queues
	- etc
- Can be stateless of stateful
	- Stateless (default) behaves as if it restarted every time they respond to an event
	- with stateful (durable functions), a context is passed to track prior activity
- Imperative (code first)
- Custom code 
- Can be monitored through Application Insights
- REST API or Visual Studio management
- Run locally or in the cloud


## Logic Apps

- Executes workflows instead of code built from pre-defined logic blocks
- Designed in a web-based designer and can execute logic triggered by services without writing any code
- Workflows are persisted in JSON schemas
- Designer-first (declarative)
- Large collection of connectors
- Many ready-made actions
- Monitor through portal or log analytics
- Manage through portal, REST API, Powershell, or Visual Studio
- Runs only in the cloud


# Describe the benefits and usage of Azure DevOps, GitHub, GitHub Actions, and Azure DevTest Labs

## DevOps Services

- Repos: source code repository for SE, DevOps, and documentation can publish code
- Boards: Agile project management system for kanban, reporting, tracking
- Pipelines: CI/CD pipeline tool
- Artifacts: hosting artiffacts, to be fed into testing or deployment pipeline steps
- Test Plans: ensure quality
- manage application development lifecycle


## Github and Github Actions

- Contribute to open source software
- Best part is the GH actions
- CI/CD toolchain - aids in the delivery, development, and management of software apps
- A little more flexible than DevOps Services
- It's a shared source-code repository, including tools that enable developers to perform code reviews by adding comments and questions in a web view of the source code before it can be merged into the main code base.
- It facilitates project management, including Kanban boards.
- It supports issue reporting, discussion, and tracking.
- It features CI/CD pipeline automation tooling.
- It includes a wiki for collaborative documentation.
- It can be run from the cloud or on-premises


## DevTest Labs

- Manage testing environments
- Automated means of managing the building, setting up, and tearing down processes for VMs that contain builds for projects
- Anything you can deploy in Azure via an ARM template can be provisioned through DevTest Labs. 
- Provisioning pre-created lab environments with their required configurations and tools already installed is a huge time saver for quality assurance professionals and developers.