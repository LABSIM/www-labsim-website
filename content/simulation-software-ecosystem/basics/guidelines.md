+++
title = "Guidelines"
date =  2019-01-15T09:50:14+01:00
weight = 32
+++


## <i class="fas fa-user"></i> Human-centered

|       |       |       |       |       |
| :---: | :---: | :--- | :---: | :---: |
| Soft real-time interactive simulation | <i class="fas fa-plus fa-2x"></i> |  {{%expand "Evaluation criteria" %}}

- simulation fidelity ;
- acceptability ;
- piloting performance ;
- agency ;
- neuro-ergonomy ;
- sense of control ;
- multi-agent / collaborative UI ;
- ...

{{% /expand%}} |  <i class="fas fa-equals fa-2x"></i> | __Virtual Reality__  |

---

## <i class="fas fa-bolt"></i> Performance focused

Because we are :

- studying the effect of various latencies on the human sense of control over an automated system (agency) ;
- prototyping a representative flight dynamic mode requiring regular continuous time clock and tight time resolution ;
- exploring the optimality of a movement produced by the human motricity system during a specific piloting task ;
- dealing with humans in a simulated virtual environment.

*Then performance __MUST BE__ a critical metric*.

---

## <i class="fas fa-code"></i> Code-less

*__Code-less__* by abstracting the hardware integration problematic & providing a LABSIM SaaS (Simulation as a Service) *"whitebox"*.

![SaaS][1]

*__Code-less__* by leveraging the software development problematic & providing a LABSIM Generic model API.

![API][2]

*__Code-less__* by providing a rich set of LABSIM Tooling platform adapted to the user confidence :

|  <i class="fas fa-user-graduate"></i> Scientist | <i class="fas fa-user-astronaut"></i> Hacker |
| --- | --- |
| A performant WYSIWYG (What You See Is What You Get) tool to setup a simulation quickly | A DIY (Do It Yourself) pipeline shortcut through a fully XML-based environment to setup a simulation like a pro ! |

---

## <i class="fas fa-graduation-cap"></i> Multi-disciplinar

![multi-disciplinar][3]

---

## <i class="fas fa-th"></i> Modular

![modular][4]

{{%attachments title="Official presentation" style="grey" pattern=".*(pdf)"/%}}

[1]: ../../../images/png/hw_sim_whitebox.png
[2]: ../../../images/png/multidisciplinar_sim_composition-0.png
[3]: ../../../images/png/multidisciplinar_sim_composition-5.png
[4]: ../../../images/png/sim_to_sim_arch_composition-4.png
