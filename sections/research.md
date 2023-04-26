<div class="block-title"><h3>Curiosity-driven AI and IoT Research</h3></div>
<br>

<div class="accordion accordion-flush" id="researchAccordion">
<!-- Put the accordion item below this line -->
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingOneRes">
      <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOneRes" aria-expanded="true" aria-controls="collapseOneRes">
        Mobile Computing and its infrastructure support
      </button>
    </h2>
    <div id="collapseOneRes" class="accordion-collapse collapse show" aria-labelledby="headingOneRes" data-bs-parent="#researchAccordion">
      <div class="accordion-body">
      
**1. Mobile Crowd Sourced Sensing** leverages large numbers of mobile devices with data collecting capabilities to provide input for Smarter Planet applications. It seeks to build a common infrastructure that interacts with devices, configures their data gathering activities based on declarative requirements from backend applications

**2. Crowdedness Detection** allows mobile devices to quickly and efficiently identify most of the neighbors by leveraging the knowledge of each other. It provides a basic function that enables interactive user experience in many Mobile Crowdsensing applications.
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingTwoRes">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseTwoRes" aria-expanded="false" aria-controls="collapseTwoRes">
        Cloud and wide area messaging
      </button>
    </h2>
    <div id="collapseTwoRes" class="accordion-collapse collapse" aria-labelledby="headingTwoRes" data-bs-parent="#researchAccordion">
      <div class="accordion-body">

**1. Cloud based publish/subscribe service** exploits the natural skewness in data distribution to provide a scalable and elastic attribute-based pub/sub service that has linear capacity scaling and multi-fold higher throughput than existing systems.

**2. Responsive, Reliable and Real-Time Messaging** delivers critical and time-sensitive information across wide area networks among end points in physical and digital worlds. It adopts multiple techniques to discover reliable routing paths and schedule message deliveries in time.
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingThreeRes">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseThreeRes" aria-expanded="false" aria-controls="collapseThreeRes">
         Distributed Stream Processing Systems
      </button>
    </h2>
    <div id="collapseThreeRes" class="accordion-collapse collapse" aria-labelledby="headingThreeRes" data-bs-parent="#researchAccordion">
      <div class="accordion-body">

**1. Hybrid high availability** addresses "transient unavailability" in stream processing systems by intelligently switching between active and passive standby mechanisms. It reduces recovery time by two-thirds and message overhead by 80%, and reproduces results as if no failure had happened.

**2. Cooperative Stream Processing** enables multiple autonomous stream processing systems to collaborate and further scale up the processing capabilities. It enables analysis and processing that are difficult or impossible in individual systems.

**3. Federated Resource Discovery** provides a unified search interface so that stream processing applications can locate and utilize resources in different autonomous systems over wide area networks.

**4. Data Source Management** discovers and allocates data sources for stream processing applications. It maintains the characteristic descriptions of potentially millions of data sources, and select the most suitable ones given applications' requirements.

**5. Negotiation Management** decides the optimal schedule for reserving remote resources among stream processing systems, such that an application execution plan can be satisfied within the required budget and time constraints.
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingFourRes">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseFourRes" aria-expanded="false" aria-controls="collapseFourRes">
        Sensor Network Data Forwarding
      </button>
    </h2>
    <div id="collapseFourRes" class="accordion-collapse collapse" aria-labelledby="headingFourRes" data-bs-parent="#researchAccordion">
      <div class="accordion-body">

### 1. Gradient Broadcast (GRAB) in sensor networks

#### Abstract:

GRAB addresses the reliable deliver of sensing data through a vast field of small, vulnerable sensors which may fail frequently and communicate via lossy wireless links. We propose a new set of mechanisms and protocols which is designed specifically for robust data delivery for large scale sensor networks in a harsh or even hostile environment. GRAB first builds and maintains a cost field, providing each sensor the direction to forward sensing data. It then forwards data along a band of _interleaved mesh_ from each source to the receiver. GRAB controls the width of the band by the amount of _credit_ carried in each data message, allowing the sender to adjust the robustness of data delivery.  The design harnesses the advantage of large scale and relies on the collective efforts of multiple nodes to deliver data, without dependency on any individual ones. We have evaluated the GRAB performance through both analysis and extensive simulation. Our analysis shows quantitatively the advantage of interleaved mesh over multiple parallel paths. Our simulation further confirms the analysis results and shows that GRAB can successfully deliver over 90% of packets over 30 hops with relatively low energy cost,  even under the adverse conditions of 30% node failures compounded with 15% link message losses.  
 

#### Idea:

\- Build a cost field for the sink. Each node keeps a cost of sending a packet to the sink via some path (ideally the minimum cost path). All costs of the nodes form the cost field. If we imagine that each node is elevated to a height equivalent to its cost, the whole cost field would look like a funnel: the sink sits at the bottom, while nodes farther to the sink are "higher".

\- Each packet carries a "credit", which is some "extra" budget that can be used to deliver a packet over a path. The total cost over the path must be smaller or equal to the total budget. Thus by controlling the amount of credit a packet carries, we effectively control the redundancy in the forwarding paths. These paths interleave and form a forwarding "mesh". The credit is the means to trade off between robustness and total cost.

**Publications:**

* Fan Ye, Gary Zhong, Songwu Lu, Lixia Zhang, ``[GRAdient Broadcast: A Robust Data Delivery Protocol for Large Scale Sensor Networks](http://irl.cs.ucla.edu/research-projects/grab-winet.ps),''  ACM Wireless Networks (WINET), Vol. 11, No.2, March 2005. (An [earlier version](/files/research/ye-ipsn-03.ps) appeared in IPSN 2003)

The old webpage for GRAB is [here](http://irl.cs.ucla.edu/GRAB/).  
 

### 2. Two-tier Data Dissemination (TTDD)

#### Abstract:

Sink mobility brings new challenges to large-scale sensor networking. It suggests that information about each mobile sink's location be continuously propagated through the sensor field to keep all sensor nodes updated with the direction of forwarding future data reports. Unfortunately frequent location updates from multiple sinks can lead to both excessive drain of sensors' limited battery power supply and increased collisions in wireless transmissions.  We propose TTDD, a Two-Tier Data Dissemination approach that provides scalable and efficient data delivery to multiple mobile sinks. Each data source in TTDD proactively builds a grid structure which enables mobile sinks to continuously receive data on the move by flooding queries within a local cell only. TTDD's design exploits the fact that sensor nodes are stationary and location-aware to construct and maintain the grid structures with low overhead. We have evaluated TTDD performance through both analysis and extensive simulation experiments. Our results show that TTDD handles multiple mobile sinks efficiently with performance comparable with that of stationary sinks.  
 

#### Idea:

\- Each source builds a virtual square grid in the network and recruits a set of nodes at grid crossings as its dissemination nodes.  A mobile sink locally floods a query within a range of a grid cell size to location nearby dissemination nodes.

\- Queries are forwarded along the grid towards the source. Data flow back in reverse direction.  Thus the impact of sinks' mobility is confined to a local area of about a cell size.

**Publications**

* Fan Ye, Haiyun Luo, Jerry Cheng, Songwu Lu, Lixia Zhang, [A Two-tier Data Dissemination Model for Large-scale Wireless Sensor Networks](/files/research/02mobicom.ps). ACM MobiCom 2002. (An extended version in ACM Mobile Applications and Networks Journal)
* A [poster](/files/research/TTDD-poster.ppt.gz) presented at SensIT PI meeting, Waltham, MA, 2002
      </div>
    </div>
  </div>
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingFiveRes">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseFiveRes" aria-expanded="false" aria-controls="collapseFiveRes">
        Energy Efficiency in Sensor Networks
      </button>
    </h2>
    <div id="collapseFiveRes" class="accordion-collapse collapse" aria-labelledby="headingFiveRes" data-bs-parent="#researchAccordion">
      <div class="accordion-body">

### 1. Probing Environment and Adaptive Sleeping (PEAS)

#### Abstract:

PEAS is a randomized energy-conservation protocol that seeks to build resilient sensor networks in the presence of frequent, unexpected node failures.  PEAS extends the network lifetime by maintaining a necessary set of working nodes and turning off redundant ones, which wake up after randomized sleeping times and replace failed ones when needed. Different from the common practice of maintaining local neighborhood topology at each node to achieve distributed coordination, PEAS has only constant state and does not require per neighbor state at any node. Each node operates based on one single piece of information. This allows PEAS to scale to very dense node deployment. PEAS is highly robust against node failures due to its simple operations and randomized design. It also ensures asymptotic connectivity.  Our simulations and analysis show that PEAS can maintain an adequate working node density in presence of as high as 38% node failures, and a roughly constant overhead of less than 1% of the total energy consumption under various deployment densities. As a result, PEAS extends a sensor network's functioning time in linear proportional to the deployed sensor population.  
 

#### Idea:

\- There's only one simple rule about which nodes can work: the distance between two neighboring working nodes should be at least Rp, which is a system parameter that determines the density of working nodes. Rp should be less than the maximum transmission range Rt to ensure connectivity of working nodes.

\- After deployment, each node first sleeps for an exponentially distributed time. When a node wakes up, it broadcasts a PROBE message within Rp. If any working nodes is within Rp, it sends back a REPLY (also within Rp). Upon hearing a REPLY, the probing node sleeps again, for another dynamically adjusted period of time; If it doesn't hear any REPLY, it starts working, until it uses up energy or fails.

**Publications**

* Fan Ye, Gary Zhong, Songwu Lu, Lixia Zhang, [PEAS: A Robust Energy Conserving Protocol for Long-lived Sensor Networks,](/files/research/ye-peas-icdcs03.ps) IEEE ICDCS 2003 (An extended version is in ACM Wireless Networks Journal).
* A [poster](/files/research/PEAS-poster.ppt.gz) presented at ICNP 2002
      </div>
    </div>
  </div>
  
  <div class="accordion-item">
    <h2 class="accordion-header" id="headingSixRes">
      <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapseSixRes" aria-expanded="false" aria-controls="collapseSixRes">
        Security in Sensor Networks
      </button>
    </h2>
    <div id="collapseSixRes" class="accordion-collapse collapse" aria-labelledby="headingSixRes" data-bs-parent="#researchAccordion">
      <div class="accordion-body">

### 1. Statistical En-route Filtering of Injected False Data (SEF)

#### Abstract:

In a large-scale sensor network individual sensors are subject to security compromises. A compromised node can inject bogus sensing reports into the network. If undetected, these bogus reports would be forwarded to the data collection point (i.e. the sink). Such attacks by compromised sensors can cause not only false alarms but also the depletion of the finite amount of energy in a battery powered network. In this paper we present a Statistical En-route Filtering (SEF) mechanism that can detect and drop such false reports. SEF requires that each sensing report be validated by multiple keyed message authentication codes (MACs), each generated by a node that detects the same event. As the report is forwarded, each node along the way verifies the correctness of the MACs probabilistically and drops those with invalid MACs at earliest points. The sink further filters out remaining false reports that escape the en-route filtering. SEF exploits the network scale to determine the truthfulness of each report through collective decision-making by multiples detecting nodes and collective false-report-detection by multiple forwarding nodes. Our analysis and simulations show that, with an overhead of 14 bytes per report, SEF is able to drop 80~90% falsely injected reports by a compromised node within 10 forwarding hops.  
 

#### Idea:

\- Divide a gloal key pool into n non-overlapping partitions.Each node pick k keys randomly from one of the n partitions. Thus only two nodes picking keys from the same partition has certain probability of sharing keys.  
\- Multiple detecting nodes each generates a keyed Message Authentication Code (MAC) and sends to an elected CoS (Center of Stimulus) node. CoS attaches the MACs to the final report - Each forwarding node has probability of possessing one of the keys used in the attached MACs, thus verifying the correctness and dropping those reports forged by attackers

**Publications**

* Fan Ye, Haiyun Luo, Songwu Lu, Lixia Zhang, ["Statistical En-route Detection and Filtering of Injected False Data in Sensor Networks,"](/files/research/sef-infocom04.pdf) to appear in IEEE INFOCOM 2004
* A [poster](../sef-sensys.ppt.gz) and [extended abstract](http://irl.cs.ucla.edu/papers/sensys03-poster.ps) at ACM SenSys, Los Angeles, CA, 2003

### 2. A Location Dependent Approach to Secure Report Generation in Sensor Networks

#### Abstract:

Existing sensor security mechanisms provide little protection when some nodes are compromised and secret keys revealed. Compromised nodes can inject false data about non-existent events to waste network resources in delivering them and produce false alarms that destruct the user's responsiveness to real events. To prevent these damages, we explore the ``location-awareness'' of sensors to develop a new security mechanism called Location Dependent Keys (LDK). In LDK, keys are not bind to nodes, as in most existing work, but to geographical locations. When an event happens, detecting nodes generate credentials for the report using keys binded to the event's location. By showing that the report is endorsed by such keys, reporting nodes prove they are at that location and able to observe what happens there. Thus a compromised node cannot forge reports about arbitrary remote events because it does not have the corresponding keys. We then exploit the a prior knowledge on the location properties of the sink and data delivery paths to detect and drop bogus reports en-route. Each node can estimate reports originated from which locations it may need to forward and store keys of these locations with a carefully designed probability distribution. Thus every forwarding node can detect bogus reports passing through it probabilistically. By accumulating detecting power over multiple hops, most bogus data are dropped before reaching the sink. Finally, the sink can reject the few false reports that escaped the en-route filtering, because it possesses the keys binded to all the locations.  
  
**Probabilistic Nested Marking for Traceback** identifies the exact origin of attacking packets, such that compromised insider nodes can be isolated from the network. It was the first work that addresses colluding attacks by multiple compromised nodes.
      </div>
    </div>
  </div>
</div>
