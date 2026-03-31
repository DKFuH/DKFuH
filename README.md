# Daniel Klas

I build practical tools for business logic, workflows, and operational clarity.

Currently working on [**OrgScript**](https://github.com/DKFuH/OrgScript), a human-readable, AI-friendly description language for business logic and operational systems.

![Business Logic](https://img.shields.io/badge/Business--Logic-FFD700?style=for-the-badge&logo=enterprise&logoColor=black)
![Workflow Design](https://img.shields.io/badge/Workflow--Design-238636?style=for-the-badge&logo=githubactions&logoColor=white)
![AI Friendly](https://img.shields.io/badge/AI--Friendly-0078D4?style=for-the-badge&logo=openai&logoColor=white)

---

## What OrgScript looks like

```yaml
process LeadQualification
  when lead.created
  if lead.budget < 10000
    transition lead.status -> "disqualified"
    notify sales "Budget below threshold"
    stop
  transition lead.status -> "qualified"
