<div align="left">

# ☁️ Rahul Biswas
### Cloud Infrastructure, Automation & Generative AI

*Final-Year BCA Student at Brainware University | AWS re/Start Program*

[![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)](#)
[![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)](#)
[![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)](#)

Welcome to my portfolio repository! I am passionate about bridging the gap between infrastructure automation and actionable AI. This space showcases my progression toward becoming an AWS Solutions Architect, highlighting hands-on cloud DevOps practices and cutting-edge Agentic AI development.

<br>

### 🛠️ Tech Stack & Tools

**Core Cloud Services**<br>
![EC2](https://img.shields.io/badge/EC2-FF9900?style=flat&logo=amazonaws&logoColor=white)
![S3](https://img.shields.io/badge/S3-569A31?style=flat&logo=amazons3&logoColor=white)
![RDS](https://img.shields.io/badge/RDS-527FFF?style=flat&logo=amazonrds&logoColor=white)
![DynamoDB](https://img.shields.io/badge/DynamoDB-4053D6?style=flat&logo=amazondynamodb&logoColor=white)
![VPC](https://img.shields.io/badge/VPC-8C4FFF?style=flat&logo=amazonaws&logoColor=white)
![Route53](https://img.shields.io/badge/Route_53-8C4FFF?style=flat&logo=amazonaws&logoColor=white)
![IAM](https://img.shields.io/badge/IAM-DD344C?style=flat&logo=amazonaws&logoColor=white)

**Automation, DevOps & Serverless**<br>
![Lambda](https://img.shields.io/badge/Lambda-FF9900?style=flat&logo=awslambda&logoColor=white)
![CloudFormation](https://img.shields.io/badge/CloudFormation-FF4F8B?style=flat&logo=amazonaws&logoColor=white)
![CloudWatch](https://img.shields.io/badge/CloudWatch-FF4F8B?style=flat&logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat&logo=terraform&logoColor=white)
![AWS CLI](https://img.shields.io/badge/AWS_CLI-232F3E?style=flat&logo=amazonaws&logoColor=white)

**AI & Machine Learning**<br>
![Bedrock](https://img.shields.io/badge/Bedrock-232F3E?style=flat&logo=amazonaws&logoColor=white)
![SageMaker](https://img.shields.io/badge/SageMaker-FF9900?style=flat&logo=amazonaws&logoColor=white)

**Development & OS**<br>
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat&logo=gnubash&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=flat&logo=visualstudiocode&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat&logo=postman&logoColor=white)

</div>

---

<br>

## 🚀 Featured Project: Executable Intelligence
**The Autonomous AI Agentic Framework**

> *Moving AI from a passive conversational chatbot to an active, secure infrastructure executor.*

**The Challenge:** Mid-to-large enterprise IT departments manage complex cloud infrastructures where DevOps engineers are often overwhelmed by repetitive "toil" (manual log analysis, script debugging, resource tagging). Current automation is often "brittle," relying on static scripts that break easily.

**The Architecture & Solution:**
Designed an AI-driven framework that utilizes LLMs to interpret high-level human goals, plan technical actions, and generate the necessary code to execute them securely.
*   **Reasoning Engine:** Utilizes Reinforcement Learning from Human Feedback (RLHF) and Supervised Learning in a strict **Plan-Act-Verify** loop.
*   **Orchestration:** **Amazon Bedrock** serves as the core layer accessing Foundation Models.
*   **Context & Execution:** **Amazon Comprehend** handles sentiment/entity recognition for urgency, while **AWS Lambda** and **Step Functions** provide the serverless execution environment and state machine logic.

**Prototyping & Security (AWS PartyRock):**
Built a functional prototype to test "Prompt-to-Action" logic. 
*   **Refinement:** Shifted from Zero-Shot to **Few-Shot prompting**, reducing hallucinations (like outdated Python libraries) and increasing the agent's logic success rate from **70% to 92%**.
*   **Guardrails:** Integrated strict execution boundaries, ensuring the AI cannot access root directories or modify sensitive AWS IAM policies without a secondary human *"Approval Gate."*

### 📈 Business Impact
| Metric | Impact |
| :--- | :--- |
| ⚡ **Efficiency** | Reduces time spent on routine troubleshooting by **~60%**. |
| 🛡️ **Accuracy** | The "Verify" loop ensures only successful operations finalize in production. |
| 📈 **Scalability** | Allows small IT teams to manage complex environments without linear headcount scaling. |

<br>

---

<br>

## 📚 AWS re/Start Curriculum & Skill Validation

*The following outlines the core competencies and hands-on labs completed during the rigorous AWS re/Start program.*

<details>
<summary><b>🐧 Linux & Operating Systems (Click to Expand)</b></summary>
<br>

*   **Command Line Mastery:** Advanced file system management, file permissions, and directory structuring.
*   **Scripting & Automation:** Wrote and executed Bash shell scripts to automate repetitive system tasks.
*   **System Administration:** Managed Linux processes, services, software packages, user groups, and log files for auditing.
</details>

<details>
<summary><b>🌐 Networking, Security & Cloud Foundations (Click to Expand)</b></summary>
<br>

*   **Core Architecture:** Navigated the AWS Infrastructure Overview, Pricing Fundamentals, and the AWS Shared Responsibility Model.
*   **Virtual Private Cloud (VPC):** Configured subnets, routing tables, and gateways. Managed VPC connectivity options and secured networks.
*   **Identity & Access:** Deep dive into IAM policies, roles, and securing cloud resources across an organization.
</details>

<details>
<summary><b>🖥️ Compute, Storage & Databases (Click to Expand)</b></summary>
<br>

*   **Elastic Compute:** Launched, secured, and troubleshot Amazon EC2 instances; deployed applications via AWS Elastic Beanstalk.
*   **Storage Solutions:** Managed Amazon S3 lifecycle policies, hosted static websites, and configured block/file storage using Amazon EBS and EFS.
*   **Database Migration:** Evaluated Amazon Aurora and Redshift; successfully migrated databases using AWS DMS and Amazon RDS.
</details>

<details>
<summary><b>⚙️ Systems Operations, Automation & Serverless (Click to Expand)</b></summary>
<br>

*   **Infrastructure as Code (IaC):** Automated deployments using AWS CloudFormation (JSON/YAML) and EC2 Launch Templates.
*   **Fleet Management:** Managed and patched instances at scale using AWS Systems Manager and the AWS CLI.
*   **Modern Workflows:** Designed serverless, event-driven architectures with AWS Lambda, Step Functions, and Amazon API Gateway.
</details>

<details>
<summary><b>🛡️ Monitoring & Governance (Click to Expand)</b></summary>
<br>

*   **Observability:** Set up alarms and monitored infrastructure health using Amazon CloudWatch.
*   **Auditing:** Tracked API activity and secured account environments using AWS CloudTrail.
*   **Data Analysis:** Integrated AWS services to query and analyze logs efficiently using Amazon Athena.
</details>

<br>

---

<br>

<div align="center">
  <h3>📫 Let's Connect</h3>
  <p>I'm always open to discussing Cloud Architecture, Agentic AI, or DevOps opportunities.</p>
  
  [![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](#)
  [![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/RahulBiswas224)
  [![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](#)
</div>
