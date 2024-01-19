# English Version

This project was developed for the subject 'Introdução a Sistemas Autónomos e Inteligentes' by the students [André Sousa](https://github.com/anfisou), [David Scarin](https://github.com/davidmscarin) and [Paulo Silva](https://github.com/WrekingPanda).

The goal of this project was to develop an environment where multiple independent agents could interact in order to complete a task. In this environment we have multiple distribuition hubs that generate packages and need them to be delivered in various locations, for that they rely on multiple drone agents to make the delivery. All agents are able to reach decision autonomously and comunicate their intentions with each other.

The script "multi_agent_drone_system.py" simulates a network of Drone and Hub agents using SPADE and an XMPP serve for communication. The Hubs store packages and communicate with Drone Agents to pick them up and deliver them to their location. The Drone agents also communicate between themselves to coordinate deliveries, avoid crashes and help with random problems.

When a hub receives a new package, they inquire all the drones about their availability to make such delivery, then decide 
wich drone should do it and communicate with him that he has been assigned that task.

Drone carrying multiple packages at once may sometimes drop some packages. When this happens, they inform the rest of the network of drones that they need help and carry out a similar process described before, but without any interference from any hub agent.

All of the information about the deliveries, positions and agent attributes are stored in the Environment which the Agents can interact with, perceive and change.

While running the script various lines are printed to the terminal detailing what is happening in the simulation, including positions of the agents, their current tasks and statuses and communications between them. At the end of the runtime some metrics used to evaluate the drone's performance will be displayed as a bar graph as well as a 3D animation of the drone's movements during this iteration of the code using matplotlib. Furthermore, there will be displayed a graphical interface with descriptive icons using pygame.

Files needed:
- multi_agent_drone_system.py: main script
- Interface.py: script to display the interface
- wireframe.py: script to implement the wireframe for the interface
- images: image folder


# Versão Portuguesa

Este projeto foi desenvolvido no âmbito da unidade curricular 'Introdução a Sistemas Autónomos e Inteligentes' pelos alunos [André Sousa](https://github.com/anfisou), [David Scarin](https://github.com/davidmscarin) e [Paulo Silva](https://github.com/WrekingPanda).

O objetivo deste projeto era desenvolver um ambiente onde múltiplos agentes autónomos pudessem interagir para completar uma tarefa. Neste ambiente, temos vários centros de distribuição que geram encomendas que precisam de ser entregues em variados locais, para isso, contam com a ajuda de múltiplos agentes de drones para realizar a entrega. Todos os agentes são capazes de tomar decisões autonomamente e comunicar as suas intenções entre si.

O script "multi_agent_drone_system.py" simula uma rede de agentes de Drone e Hub usando SPADE e um servidor XMPP para comunicação. Os Hubs armazenam as encomendas e comunicam com os drones para as levantar e entregar em seus destinos. Os agentes de drone também se comunicam entre si para coordenar entregas, evitar colisões e ajudar em problemas aleatórios.

Quando um hub recebe um novo pacote, ele interroga todos os drones sobre sua disponibilidade para realizar a entrega, decide qual drone deve fazê-lo e informa-o que foi designado para essa tarefa.

Drones que carregam várias encomendas de uma vez podem, às vezes, deixar cair algumas. Quando isso acontece, eles informam o restante da rede de drones que precisam de ajuda e realizam um processo semelhante ao descrito anteriormente, mas sem qualquer interferência de nenhum hub.

Todas as informações sobre entregas, posições e atributos dos agentes são armazenadas no ambiente com o qual os agentes podem interagir, perceber e modificar.

Ao executar o script, várias linhas são impressas no terminal detalhando o que está acontecendo na simulação, incluindo posições dos agentes, suas tarefas e status atuais, e comunicações entre eles. No final da execução, algumas métricas usadas para avaliar o desempenho dos drones serão exibidas como um gráfico de barras, assim como uma animação 3D dos movimentos dos drones durante esta iteração do código usando o matplotlib. Além disso, será exibida uma interface gráfica com ícones descritivos usando o pygame.

Ficheiros necessários:
- multi_agent_drone_system.py: script principal
- Interface.py: script para exibir a interface gráfica
- wireframe.py: script para implementar a wireframe da interface interface
- images: pasta de imagens
