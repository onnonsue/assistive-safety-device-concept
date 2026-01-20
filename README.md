# Assistive Safety Device for Vulnerable Individuals  
**A Proximity-Based, Escalation-Aware Safety System Using Beacon Technology**

---

## 1. Background & Motivation

Large-scale public spaces such as **theme parks, airports, exhibitions, and transit hubs** present persistent safety challenges for vulnerable populations, including **children, elderly individuals with cognitive impairment, and non-verbal users**.

Safety incidents in these environments rarely stem from a single failure. Instead, they often emerge from a combination of:
- temporary separation from guardians,
- limited ability to verbally communicate distress,
- delayed recognition of risk by surrounding staff.

Conventional safety solutions primarily rely on **continuous location tracking**, prioritizing positional accuracy. However, such approaches introduce **privacy concerns, battery constraints, false alarms**, and high operational complexity—making them poorly suited for vulnerable users in safety-critical contexts.

This project reframes safety not as a continuous tracking problem, but as a **contextual, event-driven interaction problem**.

---

## 2. Problem Statement

Existing assistive safety systems suffer from several limitations:

- **Verbal dependency**: Many systems assume users can clearly explain their situation.
- **Delayed intervention**: Emergencies are often detected only after escalation.
- **Over-engineered designs**: Feature-heavy devices reduce accessibility for children and cognitively impaired users.
- **Lack of semantic context**: Raw coordinates fail to convey meaningful safety states.

There is a need for a system that:
- enables **intentional, low-effort help requests**,
- minimizes false positives,
- integrates naturally with **human staff intervention workflows**.

---

## 3. Key Insight: Why Beacons Matter

This project leverages a critical characteristic of **Bluetooth Low Energy (BLE) beacons**:

> **Beacons only respond at close proximity.**

Rather than treating this as a limitation, proximity is interpreted as a **semantic signal**.

### Advantages of Beacon-Based Proximity Sensing
- **Intentionality**: Approaching a beacon-equipped location implies deliberate action.
- **Privacy-preserving**: No continuous tracking or precise coordinate logging.
- **Energy efficiency**: Suitable for low-power wearable devices.
- **Indoor robustness**: Reliable in GPS-denied environments.
- **Low infrastructure cost**: Scalable deployment in public venues.

By associating beacons with predefined **Safety Nodes** (e.g., benches, water fountains, rest areas), proximity becomes an indicator of **contextual safety states**, not merely spatial location.

---

## 4. System Concept Overview

The proposed system consists of:
- A **wearable assistive device** with a single physical button
- Beacon-equipped **Safety Nodes** distributed throughout the venue
- A **multi-stage alert escalation mechanism**
- Integration with guardian devices and on-site staff systems

### Safety Nodes (Examples)
- Benches
- Rest areas
- Water fountains
- Information desks
- Facility entrances

Reaching a Safety Node is treated as a **meaningful state transition**, such as *“reached a safe, staff-accessible area.”*

---

## 5. Interaction & Escalation Design

The system employs **progressive escalation through minimal interaction**:

1. **Proximity Detection**
   - User approaches a Safety Node
   - Guardian receives a semantic alert (e.g., *“Child is near A-1 Rest Area”*)

2. **Single Button Press**
   - Explicit location sharing
   - Indicates need for attention

3. **Double Press**
   - Emergency alert to guardian
   - Elevated urgency signaling

4. **Repeated Presses**
   - Automatic escalation to central operations
   - Nearest trained staff are dispatched

This design ensures:
- **Fail-safe behavior**
- **Low cognitive load**
- **Human-in-the-loop intervention** before situations deteriorate

---

## 6. Target Users

- Children in crowded public spaces
- Elderly individuals with dementia or cognitive decline
- Non-verbal users or individuals facing language barriers

The system avoids reliance on screens, menus, or speech recognition.

---

## 7. Research Contributions

This project contributes to research in:
- **Human-Centered Assistive System Design**
- **Context-Aware Safety Systems**
- **Event-Driven Emergency Response**
- **Semantic Localization**
- **Uncertainty-Aware Escalation Models**

Rather than optimizing positional accuracy, the system prioritizes:

> **Reliability, interpretability, and timely human intervention.**

---

## 8. Design Constraints

- **Cost target**: approximately $50 per device
- **Minimal UI**: single-button interaction
- **Robustness over feature richness**
- **Compatibility with staff-based safety operations**

---

## 9. System Architecture

### Components
1. **Wearable Assistive Device**
2. **Beacon-Based Safety Nodes**
3. **Guardian Interface**
4. **Central Operations & Staff Dispatch System**

The system operates as a **distributed, event-driven architecture**, activated through proximity events and intentional user interaction rather than continuous tracking.

### Data & Event Flow
1. Proximity detection at Safety Node  
2. Semantic location event generated  
3. Button interaction escalates alert level  
4. Guardian notified  
5. Central operations engaged if necessary  

This pipeline minimizes false alarms while ensuring timely intervention.

---

## 10. Related Work Positioning

### Continuous Localization Systems
- GPS-based child tracking
- Wi-Fi / UWB indoor positioning

**Limitations**:
- High energy consumption
- Privacy concerns
- Localization noise and false positives
- Poor interpretability

---

### Panic Button & SOS Devices
- Emergency buttons
- Elderly alert wearables

**Limitations**:
- Binary alert states
- No contextual awareness
- High cognitive burden under stress

---

### Context-Aware Smart Environments
- Sensor fusion
- AI-based activity recognition

**Limitations**:
- Infrastructure-heavy
- Limited scalability
- Opaque decision logic

---

### Positioning of This Work

This system introduces:
- **Proximity-based semantic localization**
- **Multi-stage escalation via intentional interaction**
- **Low-complexity, human-centered design**

The focus shifts from positional accuracy to **operational safety effectiveness**.

---

## 11. Why Not GPS or UWB?

| Technology | Strengths | Limitations in This Context |
|---------|----------|-----------------------------|
| GPS | Global coverage | Poor indoor accuracy, high power consumption |
| Wi-Fi | Existing infrastructure | Signal instability, privacy issues |
| UWB | High precision | Costly, complex calibration, excessive for safety signaling |
| **BLE Beacons** | Low power, proximity-based | Limited range (intentional by design) |

Safety-critical assistive systems do not require centimeter-level accuracy.  
They require **timely, meaningful intervention**.

---

## 12. Evaluation Plan

### Evaluation Objectives
- Reduce response time
- Reduce false alarms
- Ensure usability for vulnerable users

---

### Experimental Design

#### 1. Scenario-Based Simulation
- Guardian separation
- Delayed recognition
- Staff intervention

Metrics:
- Time-to-first-alert
- Time-to-human-intervention
- Escalation accuracy

---

#### 2. Comparative Baseline Study
Compared against:
- Continuous GPS tracking
- Single-stage panic button systems

Metrics:
- False positive rate
- Missed intervention rate
- Battery consumption

---

#### 3. User Interaction Study
Participants:
- Children (supervised)
- Elderly users
- Caregivers

Metrics:
- Button press success rate
- Interaction error rate
- Perceived usability (Likert scale)

---

#### 4. Staff Response Evaluation
- Staff reaction time
- Task assignment accuracy
- Operational workload impact

---

## 13. Research Scope Note

This work intentionally avoids:
- optimizing localization precision,
- fully automated safety decision-making.

Instead, it emphasizes:

> **Fail-safe design and human-centered escalation in safety-critical environments.**

---

## 14. Current Status

- Concept validation and research planning stage
- System architecture and interaction flow defined
- Preparing for simulation and pilot deployment
