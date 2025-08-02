# AI-Crisis-Manager

AI-Crisis-Manager is a multi agent prompt engineering based Project made to aid help decision makers during the times of Crisis.


## Features

- Multi Agent Architecture : 
    
    Coordinates multiple LLM agents with defined roles to simulate human decision-making in crisis scenarios.
- Explainable Output Flow :

    Every agent's output is traceable, auditable, and easy to inspect ensuring transparency in recommendations.
- Risk Evaluation Module :

    Generates threat matrices with severity scores and labels (e.g., political, humanitarian, environmental).

- Ethical Review Layer :

    Integrates a moral/ethical reasoning agent to flag or block decisions that violate humanitarian or legal standards.

- Strategy Planner Agent :

    Suggests short and long term actions tailored to the crisis situation, based on inputs from other agents.
- Supervisor Agent :

    Final reviewer that integrates all outputs and generates the consolidated response for human decision-makers.


## 🧩 Agents

Each agent has a distinct role and uses a custom prompt to guide its behavior:

| Agent Name         | Role Description                                       |
|--------------------|--------------------------------------------------------|
| `Summarizer`       | Condenses incoming information (news, reports, etc.)   |
| `RiskAssessor`     | Identifies threats and assigns severity ratings        |
| `EthicalReviewer`  | Checks proposed actions against ethical considerations |
| `Planner`          | Recommends strategic actions and next steps            |
| `Supervisor`       | Oversees and validates outputs of all other agents     |

## Estimated Token Usage per Agent


| 🧠 Agent                  | 📝 Prompt Type                  | 🔤 Prompt Tokens | 📥 Expected Input Tokens | 📦 Total Tokens Per Cycle |
|--------------------------|----------------------------------|------------------|---------------------------|----------------------------|
| Summarizer Agent         | Instruction + Sample             | ~250             | ~2,000 (report input)     | ~2,250                     |
| Risk Assessor Agent      | Risk schema + guidelines         | ~300             | ~1,500 (from summarizer)  | ~1,800                     |
| Planner Agent            | Strategic planning rules         | ~350             | ~1,500                    | ~1,850                     |
| Ethical Reviewer Agent   | Ethical evaluation checklist     | ~400             | ~1,000                    | ~1,400                     |
| Supervisor Agent         | Final analysis prompt            | ~200             | ~2,000 (collated inputs)  | ~2,200                     |

> ⚠️ **Note:** Token estimates are approximate and may vary depending on the crisis context and response length. Outputs are designed to stay under 3,000 tokens per agent per cycle.

## License

[MIT](https://choosealicense.com/licenses/mit/)
