# Projeto de Pesquisa

Desenvolvimento de Modelos de Reconhecimento Facial para Computação Assistiva

Coordenador: Prof. Lucio Agostinho Rocha - Universidade Tecnológica Federal do Paraná -  câmpus Apucarana

### Demonstração: https://www.youtube.com/watch?v=-7l3UtnLoJE

### Código baseado em: https://www.pyimagesearch.com/2019/03/11/liveness-detection-with-opencv/

### Como executar:

1. Criar as pastas 'dataset/real' e 'dataset/fake'

2. Criar a pasta 'videos'

3. Gerar um pequeno video '/videos/real.mov' com a imagem válida.

4. Gerar um pequeno vídeo '/videos/fake.mp4' com a imagem inválida.

5. Executar a sequencia de comandos:

```
# python gather_examples.py --input videos/real.mov --output dataset/real --detector face_detector --skip 1
# python gather_examples.py --input videos/fake.mp4 --output dataset/fake --detector face_detector --skip 4
# python train.py --dataset dataset --model liveness.model --le le.pickle
# python liveness_demo.py --model liveness.model --le le.pickle --detector face_detector
```