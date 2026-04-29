# INTRODUCTION TO ARTIFICIAL INTELLIGENCE

## Definition of AI

Artificial Intelligence (AI) is a branch of computer science concerned with the construction of computational systems that implement functions mapping inputs to outputs in a manner that approximates or exceeds human performance on tasks requiring perception, inference, learning, or decision-making. Such systems are instantiated through algorithms, typically parameterized models, whose behavior is derived from data, rules, or a combination thereof.

---

# OBJECTIVES

- **Artificial Intelligence**: To formalize and implement computational models capable of task execution where explicit rule enumeration is impractical or infeasible.
    
- **Forms of AI**: To classify AI systems according to scope of competence and generalization capacity.
    
- **What AI Does**: To transform input data into actionable outputs via functions including classification, regression, generation, ranking, and control.
    
- **From Data Problems to AI Capabilities**: To establish a bijective mapping between problem classes (e.g., supervised learning, unsupervised learning, reinforcement learning) and solution methodologies.
    
- **Data and Its Types**: To define the structural and semantic categories of data utilized in model training and inference.
    
- **3 Eras of Processing Data**: To delineate historical transitions in how data is processed and leveraged computationally.
    
- **Future of AI**: To assess forward trajectories constrained by computational, theoretical, and regulatory limits.
    

---

## Domains Example of AI

AI systems are deployed in domains where input-output mappings are non-trivial, including natural language processing (text-to-text transformations), computer vision (image-to-label or image-to-image mappings), robotics (sensor-to-actuator control), and financial systems (time-series prediction).

---

# TYPES OF AI

## ANI (Artificial Narrow Intelligence)

A computational system whose functional competence is restricted to a single task or a finite set of closely related tasks, with no inherent capacity for transfer learning beyond its trained domain without external modification.

## AGI (Artificial General Intelligence)

A hypothetical computational system possessing the ability to perform any intellectual task that a human can perform, characterized by domain-independent generalization, adaptive reasoning, and transfer across arbitrary problem spaces.

## ASI (Artificial Superintelligence)

A hypothetical extension of AGI wherein the system’s cognitive performance strictly dominates that of humans across all measurable tasks, including those involving creativity, strategic reasoning, and scientific discovery.

---

# TYPES OF AI ON BASIS OF TASKS

## Predictive AI

A class of AI systems that estimate unknown or future values of variables by learning a function ( f: X \rightarrow Y ) from historical data, where (X) represents input features and (Y) represents target variables.

## Generative AI

A class of AI systems that model the joint probability distribution ( P(X) ) or conditional distribution ( P(X|Y) ) of data and generate new samples that are statistically consistent with the training distribution.

## Agentic AI

A class of AI systems that operate within an environment by selecting actions ( a \in A ) over time to optimize an objective function, typically defined via reward maximization or goal satisfaction, potentially incorporating planning and feedback loops.

---

# PROMPT

## Zero-shot

A condition in which a model performs a task without exposure to task-specific examples at inference time, relying solely on prior training.

## One-shot

A condition in which exactly one example is provided to specify the desired task behavior.

## Few-shot

A condition in which a finite, typically small, set of examples is provided to constrain the model’s output distribution.

## Role-based

A prompting strategy in which constraints on output form or reasoning style are imposed by specifying an assumed role, thereby conditioning response generation.

---

# DATA

## TYPES

### Structured

Data conforming to a rigid schema with fixed fields and types, enabling deterministic storage and retrieval (e.g., relational tables).

### Unstructured

Data lacking a predefined schema, where structure must be inferred computationally (e.g., free-form text, images, audio).

### Semi-structured

Data that does not conform to a strict schema but contains explicit organizational markers (e.g., key-value pairs in JSON or XML).

### Metadata

Data that encodes descriptive attributes of primary data, including provenance, format, temporal characteristics, and access constraints.

---

# 3 ERAS OF PROCESSING DATA

1. **Rule-Based Era**  
    Systems defined by explicitly encoded rules, where behavior is fully determined by human-specified logic.
    
2. **Statistical Learning Era**  
    Systems that infer patterns from data using statistical methods, enabling probabilistic predictions and generalization.
    
3. **Foundation Model Era**  
    Systems trained on large-scale, heterogeneous datasets using high-capacity models, enabling multi-task generalization with minimal task-specific adaptation.
    

---

# FUTURE OF AI

Future AI systems are expected to exhibit increased model scale, multimodal integration, and autonomy in sequential decision-making. Constraints include computational resource limits, alignment with externally specified objectives, interpretability limitations, and legal or regulatory compliance. Complete autonomy or general intelligence remains unproven and is not presently instantiated.