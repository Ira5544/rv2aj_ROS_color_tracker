# rv2aj_ROS_color_tracker
Pacotes ROS utilizados para o trabalho.


1.Extraia os arquivos compactados para a pasta src do ambiente ROS que estiver utilizando (catkin_ws, ws_moveit, etc).
2. Se estiver utilizando o catkin_ws, abra o terminal e digite: 

```
cd ~/catkin_ws
catkin_make
```

3. Se estiver utilizando o ws_moveit, abra o terminal e digite:

```
cd ~/ws_moveit
catkin build
```

4. Com o ROS inicializado, abra uma nova janela do terminal.
5. Digite:

```
cd ~/catkin_ws
source devel/setup.bash
roslaunch rv2aj_moveit_config demo.launch
```

Isso irá inicializar o URDF do braço robótico no Rviz.

6. Abra uma nova janela do terminal.

7. Digite:

```
cd ~/catkin_ws
source devel/setup.bash
rosrun color_tracker color.py
```  

8. Após garantir que as peças foram colocadas no campo de visão da sua câmera, ajuste os parâmetros HSV nas janelas que aparecerem.

Note que as janelas "imagemA", "imagemR", "imagemL", "imagemV", "imagemVr" e "imagemOB" correspondem às cores Azul, Roxo, Laranja, Verde,
Vermelho e à cor do obstáculo, respectivamente. Porém, você pode utilizar os sliders para ajustá-las para a cor de que bem desejar. 
As imagens nessa janela são binarizações do resultado da filtragem realizada.

A janela "imagem" corresponde à união das binarizações acima mencionadas.

A janela "filtros" corresponde aos parâmetros dos filtros morfológicos utilizados, sendo possível ajustar o tamanho da matriz e o número
de vezes que eles serão aplicados.

A janela "frame" mostra o que a câmera utilizada está "vendo".

Após realizar os ajustes, clique na janela "frame" e aperte a tecla S. Isso fará com que o código comece a publicar as coordenadas do
centro do contorno de cada peça.

9. Abra uma nova janela no terminal.

10. Digite:

```
cd ~/catkin_ws
source devel/setup.bash
rosrun teste teste
```

11. Abra uma nova janela no terminal.

12. Digite:

```
cd ~/catkin_ws
source devel/setup.bash
rosrun caixa plot_caixa.py
```  

13. Certifique-se de que o código de detecção de cores está rodando e publicando as coordenadas das peças!!
Irá aparecer uma janela "teste".  Clique nela e aperte R. Isso fará com que o obstáculo detectado pela câmera seja publicado no Rviz.

14. Abra uma nova janela no terminal.

15. Digite:

```
cd ~/catkin_ws
source devel/setup.bash
rosrun rviz_handler move.py
```   

16. Abra uma nova janela no terminal.

17. Digite:

```
cd ~/catkin_ws
source devel/setup.bash
rosrun rviz_handler move_teste_matriz.py
```

18.Abra uma nova janela no terminal.

19.Digite:

```
cd ~/catkin_ws
source devel/setup.bash
rosrun rviz_handler Rviz_planner.py
``` 

20.Certifique-se de que a posição do robô é a mesma do Rviz. Irá aparecer uma janela "Traj". Clique na janela e aperte "P".
Isso fará com que o planejamento de trajetória seja iniciado.
    
