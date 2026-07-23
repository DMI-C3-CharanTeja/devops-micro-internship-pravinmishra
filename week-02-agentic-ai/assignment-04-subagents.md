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

![Screenshot 1](./screenshots/assingment04_screenshot01.PNG) 

---

# Task 2 — Compare the Agent Configurations

## Goal

Analyze the configuration differences between the three agents and demonstrate understanding of model and tool selection.

### Written Answers

#### 1. Why does the cost optimizer use Haiku instead of Sonnet?

The cost optimizer performs lightweight analysis tasks such as checking Terraform resources and identifying possible cost-saving improvements. Since it does not require deep reasoning like security analysis, the faster and more cost-efficient Haiku model is suitable for this task.

---

#### 2. Why does the security auditor NOT have Write in its tools list?

The security auditor is designed only to inspect and analyze Terraform configurations. Removing Write permission prevents accidental modification of infrastructure files and follows the principle of least privilege.

---

#### 3. Why does the tf-writer use `inherit` instead of a specific model?

The Terraform writer needs flexibility because it performs code generation and modification tasks. Using inherit allows it to use the default model configuration from Claude Code instead of forcing a fixed model.

---

### Evidence

#### Screenshot 2 — `security-auditor.md` frontmatter showing model and tools configuration

![Screenshot 2](./screenshots/assingment04_screenshot02.PNG) 

---

#### Screenshot 3 — `cost-optimizer.md` frontmatter showing the model and tools configuration

![Screenshot 3](./screenshots/assingment04_screenshot03.PNG) 

---

# Task 3 — Run the Security Auditor

## Goal

Trigger the security auditor agent and analyze the generated security report for your Terraform infrastructure.

### Evidence

#### Screenshot 4 — The delegation message showing Claude launched the security-auditor

![Screenshot 4](./screenshots/assingment04_screenshot04.PNG) 

---

#### Screenshot 5 — Security audit report output

![Screenshot 5](./screenshots/assingment04_screenshot05.PNG) 

---

# Task 4 — Run the Cost Optimizer

## Goal

Trigger the cost optimizer agent and review the generated cost optimization report.

### Evidence

#### Screenshot 6 — The full cost optimization report

![Screenshot 6](./screenshots/assingment04_screenshot06.PNG) 

---

# Submission Instructions

- Ensure all agent files are committed in `.claude/agents/`
- Complete all written answers in your GitHub Repo
- Push final changes to your forked GitHub repository

---

## GitHub Repository URL

Paste your forked repository URL here:

<<<<<<< HEAD
`https://github.com/DMI-C3-CharanTeja/Ultimate-Agentic-DevOps-with-Claude-Code.git`
=======
`Add your URL here`
>>>>>>> upstream/main

---

# Completion Checklist

- [X] `.claude/agents/` folder contains all 3 agent files
- [X] Screenshot 2 shows correct `security-auditor.md` configuration
- [X] Screenshot 3 shows correct `cost-optimizer.md` configuration
- [X] All 3 written answers completed 
- [X] Security auditor executed successfully
- [X] Cost optimizer executed successfully
- [X] Security report is visible with findings
- [X] Cost report is visible with recommendations
- [X] All required screenshots added
- [X] GitHub repo updated with agents

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