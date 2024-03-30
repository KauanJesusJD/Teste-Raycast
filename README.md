# Teste-Raycast
# Criador
  Este pequeno exercício foi feito por Kauan Jesus e Arthur Victor do 3° Jogos
# Descrição
Este jogo vai simular um microlabirinto onde o personagem principal (O Blue Gut), precisa destruir as paredes no seu caminho ate chegar no fim do Labirinto demarcado por varios efeitos especiais. Esse jogo tem como exemplo demonstrar o uso simples de RayCast para destruir os objetos, além de demonstrar também o uso basíco de uma prefab. Neste readme serao explicados os passos basícos de como chegamos em nosso resultado final. No fim deste Readme havéra o link para o arquivo do jogo.
# Como foi feito os codigos
Todos os codígos utilizados foram baseados em exemplos e conceitos aprendidos em aula. Utilizamos muito dos exemplos dado pela nossa professora. Em casos onde tivemos duvidas, utilizamos a internet como apoio para conseguirmos chegar numa conclusao, mas todos os exemplos abaixos citados foi baseado em teorias praticas.
#  Movimento do personagem
Primeiro criamos uma variável para decidir a "velocidade" que o personagem andaria. Depois utilizamos o "if" para se uma tecla específica for clicada ele andaria para a frente, trás, direita e esquerda. E a tecla espaço serve para pular (eixo Y).

![image](https://github.com/lucasnoelgb/promanopicas/assets/129121307/f68bc192-2700-48ce-b5d8-7da4e685c576)

## movimento com o mouse
- Primeiro criamos uma variável para decidir a "velocidade" que a câmera irá rotacionar. O código que faz a rotação captura o movimento do mouse horizontal e vertical, e aplica a rotação ao personagem com base na variável ´rotaçao´. A rotação ocorre no eixo horizontal (eixo X) do personagem.

![image](https://github.com/lucasnoelgb/promanopicas/assets/129121307/24959082-dacd-4f76-8b54-0395fa0af8c0)

# Raycast e Destroy 
- Este é um script do Unity que detecta quando a tecla "espaco" é pressionada e dispara um raio de colisão a partir do ponto de toque do mouse na tela.
Se Input.GetKeyDown(KeyCode.Space) retornar true, um novo raio é criado a partir do ponto de toque do mouse na tela com 'Camera.main.ScreenPointToRay(Input.mousePosition)'.
O método 'Physics.Raycast' dispara o raio e retorna um objeto RaycastHit com informações sobre o objeto atingido, se houve uma colisão.
Se houve uma colisão, a condição 'hit.collider.gameObject != this.gameObject' verifica se o objeto atingido é diferente do objeto com o script atribuído.
Se o objeto atingido não for o mesmo do objeto com o script atribuído, Destroy(hit.collider.gameObject) é chamado para destruí-lo.<br>

![image](https://github.com/lucasnoelgb/promanopicas/assets/129121307/fc11fddd-e0a3-42bb-be93-1cbc8bf41035)

# Prefabs Usados
- Este é o 'Blue Gut' é o personagem que você controlara durante o percurso do labirinto. 
![image](https://github.com/lucasnoelgb/promanopicas/assets/129121307/d1ccfdd6-a071-43d5-8802-3e1f1b808e73)
- Ao terminar o Labirinto você será recebido com esse fogos de arteficios que sinalizará que o jogador acaba de terminar o percurso<br>
![image](https://github.com/lucasnoelgb/promanopicas/assets/129121307/c6469211-447d-4aa9-a858-bbad4a942a29)
![image](https://github.com/lucasnoelgb/promanopicas/assets/129121307/f3dad9bc-fbcc-4bf1-9473-a827c1709a11)
# Link do Drive
https://drive.google.com/file/d/19bZeI4K-NXSlA_uJo5K3qTIdPUvrW055/view?usp=sharing
