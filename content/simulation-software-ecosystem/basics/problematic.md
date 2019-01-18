+++
title = "Problematic"
date =  2019-01-15T09:49:57+01:00
weight = 31
+++

> *How to allow fast & early conception/evaluation cycle of innovative concept in situ ?*

This was the motivation of the very first development of the LABSIM's Simulation Software Environment (SSE). Our answer to solve the *ditto* problematic. Because Research area is a very versatile environment, we start only from this. No requirements at all.

So we began with a simple term-by-term analysis of this problematic to establish a set of requirements to met with our SSE, then we've done an graphical modeling of the initial workflow to identify bottleneck which has will finally and an estimation of a *desired* workflow.

*Let's begin*.

---

### Term-by-term analysis


> *How to allow __fast & early conception__/evaluation cycle of innovative concept in situ ?*

- rapid system prototyping ;
- cheap & affordable solution => *software simulation*.

> *How to allow __fast & early__ conception/__evaluation__ cycle of innovative concept in situ ?*

- to evaluate something, we need to be representative &/or immersive enough ;
- it also mean that we will probably have to handle a wide range of heterogeneous sensors ;
- to evaluate something we must guarantee data consistency.

> *How to allow fast & early conception/evaluation __cycle__ of innovative concept in situ ?*

- reliability ;
- repeatability.

> *How to allow fast & early conception/evaluation cycle of __innovative concept__ in situ ?*

- innovation arises from domain specific expert ;
- innovation could also emerge from a blend, a fusion of various scientific domain ;
- we do computer sciences so we should leverage this aspect from users => *focus on key competencies (reminder: initials conditions)*

> *How to allow fast & early conception/evaluation cycle of innovative concept __in situ__ ?*

- HiL (Human in the Loop) interactive simulation => *human centered design approach* ;
- generally speaking, Human does not lag. that said we should focus on performance with soft real-time requirements => ~100Hz ;
- human centered + computer science = VR (Virtual Reality) principles !
- because we are an in-house ONERA's lab, by "Human" we mean : "Pilot", "UAV/UGV/ATC operator", ...

---

### Initial Workflow

{{<mermaid align="center">}}

graph TD;

  External_0(("fa:fa-users"))

  subgraph ICNA / RFDS

    ICNA_0("Domain Expert")
    ICNA_1("System Architect")
    ICNA_2{"fa:fa-cog"}
    ICNA_3{"fa:fa-graduation-cap"}

    ICNA_0 --> |model| ICNA_2
    ICNA_1 --> |publish| ICNA_3
    ICNA_0 --> |publish| ICNA_3

  end

  subgraph LABSIM

    LABSIM_0("fa:fa-keyboard The Team")
    LABSIM_1["fa:fa-server Interactive Simulation"]
    LABSIM_2{"fa:fa-database"}

    LABSIM_0 --> LABSIM_1
    LABSIM_1 ==> |generate| LABSIM_2

  end

  External_0 --> LABSIM_1
  ICNA_1 -.-> |design experimental protocol| External_0
  ICNA_2 -.-> |integrate| LABSIM_0
  ICNA_1 -.-> |compose| LABSIM_0
  LABSIM_2 -.-> |analyze| ICNA_0
  LABSIM_2 -.-> |analyze| ICNA_1

{{< /mermaid >}}

---

### Expected Workflow

{{<mermaid align="center">}}

graph TD;

  External_0(("fa:fa-users"))
  External_1(("fa:fa-database"))

  subgraph ICNA / RFDS

    ICNA_0("Domain Expert")
    ICNA_1("System Architect")
    ICNA_2{"fa:fa-cog"}
    ICNA_3{"fa:fa-graduation-cap"}

    ICNA_0 --> |model| ICNA_2
    ICNA_1 --> |publish| ICNA_3
    ICNA_0 --> |publish| ICNA_3

  end

  subgraph LABSIM

    subgraph SSE

      SSE_0("fa:fa-magic Simulation Composition Pipeline")
      SSE_1("fa:fa-magic Model Integration Pipeline")

    end

    LABSIM_0("fa:fa-keyboard The Team")
    LABSIM_1["fa:fa-server Interactive Simulation"]
    LABSIM_3{"fa:fa-user-cog Actor" }
    LABSIM_4{"fa:fa-user-graduate Core"}

    LABSIM_0 --> SSE_0
    LABSIM_0 --> SSE_1
    SSE_0 ==> |generate| LABSIM_4
    SSE_1 ==> |generate| LABSIM_3
    LABSIM_3 --> |catalog| SSE_0
    LABSIM_3 --> LABSIM_1
    LABSIM_4 --> LABSIM_1

  end

  External_0 --> LABSIM_1
  ICNA_1 -.-> |design experimental protocol| External_0
  ICNA_2 -.-> |integrate| SSE_1
  ICNA_1 -.-> |compose| SSE_0
  LABSIM_1 ==> |generate| External_1
  External_1 -.-> |analyze| ICNA_0
  External_1 -.-> |analyze| ICNA_1

{{< /mermaid >}}

{{%attachments title="Official presentation" style="grey" pattern=".*(pdf)"/%}}
