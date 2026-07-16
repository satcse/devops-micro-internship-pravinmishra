# Assignment 4 — Building Your AI Team

Part of the DevOps Micro Internship (DMI) Cohort 3 with Agentic AI

---

## Purpose

In this assignment, you will build and configure a set of specialized AI subagents inside your project. You will learn how different models and tool permissions define agent behavior, and you will trigger two real agent delegations to analyze security and cost aspects of your Terraform infrastructure.

---

# Task 1 — Create the Agents Folder and Add Files

## Goal

Create the `.claude/agents/` directory and add all required agent files.

### Evidence

#### Screenshot 1 — VS Code sidebar showing `.claude/agents/` with all 3 files

![ClaudeAgents](screenshots/week-02-assignment-04-snapshot-01.png)

---

# Task 2 — Compare the Agent Configurations

## Goal

Analyze the configuration differences between the three agents and demonstrate understanding of model and tool selection.

### Written Answers

#### 1. Why does the cost optimizer use Haiku instead of Sonnet?

The Cost Optimizer performs lightweight analysis tasks, such as reviewing Terraform resources and identifying potential cost-saving opportunities. Since these tasks do not require deep reasoning or complex security analysis, the faster and more cost-effective Haiku model is well suited for this workload.

---

#### 2. Why does the security auditor NOT have Write in its tools list?

The Security Auditor is designed solely to inspect and analyze Terraform configurations. Removing write permissions ensures that infrastructure files cannot be modified accidentally or maliciously, while adhering to the principle of least privilege.

---

#### 3. Why does the tf-writer use `inherit` instead of a specific model?

The Terraform Writer requires flexibility because it performs code generation and modification tasks. Using `inherit` allows it to leverage the default model configuration defined in Claude Code, rather than enforcing a fixed model, enabling the agent to benefit from future model updates and configuration changes.

---

### Evidence

#### Screenshot 2 — `security-auditor.md` frontmatter showing model and tools configuration

![SecurityAuditor](screenshots/week-02-assignment-04-snapshot-02.png)
---

#### Screenshot 3 — `cost-optimizer.md` frontmatter showing the model and tools configuration

![CostOptimizer](screenshots/week-02-assignment-04-snapshot-03.png)

---

# Task 3 — Run the Security Auditor

## Goal

Trigger the security auditor agent and analyze the generated security report for your Terraform infrastructure.

### Evidence

#### Screenshot 4 — The delegation message showing Claude launched the security-auditor

![ClaudeDelegation](screenshots/week-02-assignment-04-snapshot-04.png)

---

#### Screenshot 5 — Security audit report output

![AuditReport](screenshots/week-02-assignment-04-snapshot-05.png)

---

# Task 4 — Run the Cost Optimizer

## Goal

Trigger the cost optimizer agent and review the generated cost optimization report.

### Evidence

#### Screenshot 6 — The full cost optimization report

![CostReport1](screenshots/week-02-assignment-04-snapshot-06a.png)
![CostReport2](screenshots/week-02-assignment-04-snapshot-06b.png)
![CostReport3](screenshots/week-02-assignment-04-snapshot-06c.png)

---

# Submission Instructions

- Ensure all agent files are committed in `.claude/agents/`
- Complete all written answers in your GitHub Repo
- Push final changes to your forked GitHub repository

---

## GitHub Repository URL

Paste your forked repository URL here:

https://github.com/satcse/Ultimate-Agentic-DevOps-with-Claude-Code

---

# Completion Checklist

- ✅ `.claude/agents/` folder contains all 3 agent files
- ✅ Screenshot 2 shows correct `security-auditor.md` configuration
- ✅ Screenshot 3 shows correct `cost-optimizer.md` configuration
- ✅ All 3 written answers completed 
- ✅ Security auditor executed successfully
- ✅ Cost optimizer executed successfully
- ✅ Security report is visible with findings
- ✅ Cost report is visible with recommendations
- ✅ All required screenshots added
- ✅ GitHub repo updated with agents

---

## 📌 About DMI & CloudAdvisory

DevOps Micro Internship (DMI) is a project-based DevOps program run by Pravin Mishra (The CloudAdvisory) focused on real-world execution, systems thinking, and career readiness.

It helps learners build strong DevOps foundations with hands-on experience.

---

## 📌 Resources

- 🌐 DMI Official Website: https://pravinmishra.com/dmi  
- 🎓 DevOps for Beginners (Udemy): https://www.udemy.com/course/devops-for-beginners-docker-k8s-cloud-cicd-4-projects/  
- 🎓 Agentic AI DevOps with Claude Code: https://www.udemy.com/course/ultimate-agentic-ai-devops-with-claude-code/  
- 🎓 DevOps with Claude Code: Terraform, EKS, ArgoCD & Helm: https://www.udemy.com/course/devops-with-claude-code-terraform-eks-argocd-helm/  
- ▶️ YouTube Playlist: https://www.youtube.com/playlist?list=PLFeSNDtI4Cho  
- 🔗 Pravin Mishra (LinkedIn): https://www.linkedin.com/in/pravin-mishra-aws-trainer/  
- 🏢 CloudAdvisory (LinkedIn): https://www.linkedin.com/company/thecloudadvisory/

---

*This submission is part of DevOps Micro Internship (DMI) Cohort 3 — Agentic AI Track.*