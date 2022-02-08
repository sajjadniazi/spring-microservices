<p><strong>Introduction </strong></p>
<p>In this project I am establishing connection between two microservices that is currency services and currency conversion microservices. I am Using Eureka Naming server for service discovery, Feign Client as a declarative web service Client. Rabbit MQ, Zipkin and Spring Cloud Sleuth for distributed Tracing and Resilience4j as a circuit breaker.</p>
<p><strong>Prerequisites</strong></p>
<ul>
<li>You should know Java and Spring.</li>
<li>A basic Knowledge of developing web applications is a plus but NOT mandatory.</li>
<li>A basic Knowledge of Spring Boot is a plus but NOT mandatory.</li>
<li>A basic Knowledge of JPA is a Plus but NOT mandatory.</li>
<li>A basic Knowledge, Maven or Tomcat.</li>
</ul>
<p><strong>Installing Tools</strong></p>
<ul>
<li>Eclipse &amp; Embedded Maven</li>
<li>Rest Client</li>
<li>Git - <a href="https://git-scm.com/">https://git-scm.com/</a></li>
<li>Rabbit MQ - <a href="https://www.rabbitmq.com/download.html">https://www.rabbitmq.com/download.html</a></li>
<li>ZipKin - <a href="https://zipkin.io/">https://zipkin.io/</a></li>
</ul>
<p><strong>Installing Rabbit MQ</strong>&nbsp;</p>
<ul>
<li><u><a href="https://www.rabbitmq.com/install-windows.html">https://www.rabbitmq.com/install-windows.html</a></u></li>
<li><u><a href="https://www.rabbitmq.com/which-erlang.html">https://www.rabbitmq.com/which-erlang.html</a></u></li>
<li><u><a href="http://www.erlang.org/downloads">http://www.erlang.org/downloads</a></u><strong>&nbsp;</strong></li>
</ul>
<p><strong>Services URLs</strong></p>
<p><strong>Currency Exchange Service</strong></p>
<p><a href="http://localhost:8000/currency-exchange/from/USD/to/PKR">http://localhost:8000/currency-exchange/from/USD/to/PKR</a></p>
<img src="https://user-images.githubusercontent.com/25585558/152929786-cacb888b-5253-4f1a-afa9-dada88fd5311.png" alt="" /></p>
<p><strong>Currency Conversion Service</strong></p>
<p><a href="http://localhost:8100/currency-conversion/from/USD/to/PKR/quantity/10">http://localhost:8100/currency-conversion/from/USD/to/PKR/quantity/10</a></p>
<img src="https://user-images.githubusercontent.com/25585558/152930166-3310dc0d-6c7b-4909-b6bf-21a8f73d4e3c.png" alt="" /></p>
<p><a href="http://localhost:8100/currency-conversion-feign/from/USD/to/PKR/quantity/10">http://localhost:8100/currency-conversion-feign/from/USD/to/PKR/quantity/10</a></p>
<img src="https://user-images.githubusercontent.com/25585558/152930272-20357307-3fb2-4d7c-a40d-6a08d3956616.png" alt="" /></p>
<p><strong>Eureka</strong></p>
<p><a href="http://localhost:8761/">http://localhost:8761/</a></p>
<img src="https://user-images.githubusercontent.com/25585558/152930328-cdfed725-91ef-4f98-9182-0a20d863560c.png" alt="" /></p>
<p><strong>Zipkin</strong></p>
<p><a href="http://localhost:9411/zipkin/?lookback=15m&amp;endTs=1644222113529&amp;limit=10">http://localhost:9411/zipkin/?lookback=15m&amp;endTs=1644222113529&amp;limit=10</a></p>
<img src="https://user-images.githubusercontent.com/25585558/152930599-cbbf29c9-6967-4332-9c1e-5aad3a2d6402.png" alt="" /></p>
<p>&nbsp;</p>
<p><strong>Spring Cloud API Gateway</strong></p>
<p><a href="http://localhost:8765/currency-exchange/from/USD/to/PKR">http://localhost:8765/currency-exchange/from/USD/to/PKR</a></p>
<img src="https://user-images.githubusercontent.com/25585558/152930692-63008057-7eb0-4989-bd6a-91279066d91c.png" alt="" /></p>
<p><a href="http://localhost:8765/currency-conversion/from/USD/to/PKR/quantity/10">http://localhost:8765/currency-conversion/from/USD/to/PKR/quantity/10</a></p>
<p><a href="http://localhost:8765/currency-conversion-feign/from/USD/to/PKR/quantity/10">http://localhost:8765/currency-conversion-feign/from/USD/to/PKR/quantity/10</a></p>
<p><a href="http://localhost:8765/currency-conversion-new/from/USD/to/PKR/quantity/10">http://localhost:8765/currency-conversion-new/from/USD/to/PKR/quantity/10</a></p>
<p><strong>Running Examples</strong></p>
<p>Download the zip or clone the Git repository.</p>
<p>Unzip the zip file (if you downloaded one).</p>
<p>Make sure you start the services in this order (a)naming-server (b)api-gateway-server (c)currency-exchange-service (d)currency-conversion-service and zipkin.jar</p>
<p>if you are using windows rabbit MQ will be up and running by default</p>
<p>Command to run on windows</p>
<p>SET RABBIT_URI=amqp://localhost</p>
<p>java -jar zipkin-server-2.5.2-exec.jar</p>
