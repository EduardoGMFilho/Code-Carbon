# Code-Carbon

# Tutorial: Usando o CodeCarbon

## 1. O que é o CodeCarbon

O **CodeCarbon** é uma ferramenta que ajuda a medir o impacto ambiental de programas de computador.
Ele estima quanta energia o computador consumiu durante a execução de um código e converte esse
consumo em uma estimativa de **emissão de CO₂**.

Em termos simples, o CodeCarbon mostra o quanto um programa pode impactar o meio ambiente enquanto roda.

---

## 2. Por que isso é importante para TI Verde

Na área de TI, computadores, servidores e sistemas funcionam por longos períodos e consomem muita energia.
Quanto maior o consumo, maior o impacto ambiental.

Com o CodeCarbon, é possível:
- Comparar códigos mais eficientes e menos eficientes
- Reduzir desperdício de energia
- Tornar sistemas mais sustentáveis
- Incluir o impacto ambiental nas decisões técnicas

---

## 3. Pré-requisitos

Antes de começar, você precisa ter:
- Python 3.8 ou superior
- Um editor de código (VS Code, por exemplo)
- Acesso ao terminal

Para verificar a versão do Python:
```bash
python --version
```

---

## 4. Instalação do CodeCarbon

Instale a biblioteca com o comando:
```bash
pip install codecarbon
```

---

## 5. Exemplo Prático de TI Verde

Este exemplo compara duas formas de executar a mesma tarefa:
uma menos eficiente e outra mais eficiente.

### 5.1 Código menos eficiente

```python
from codecarbon import EmissionsTracker

tracker = EmissionsTracker(project_name="Processamento Não Otimizado")
tracker.start()

resultado = []
for i in range(5_000_000):
    resultado.append(i * 2)

emissions = tracker.stop()
print(f"Emissões estimadas: {emissions} kg de CO2")
```

---

### 5.2 Código mais eficiente

```python
from codecarbon import EmissionsTracker

tracker = EmissionsTracker(project_name="Processamento Otimizado")
tracker.start()

resultado = [i * 2 for i in range(5_000_000)]

emissions = tracker.stop()
print(f"Emissões estimadas: {emissions} kg de CO2")
```

---

### 5.3 Análise

- O código otimizado executa mais rápido
- Menor tempo de execução reduz o consumo de energia
- Menor consumo de energia reduz o impacto ambiental

Esse é um princípio central da **TI Verde**.

---

## 6. Relatórios Gerados

O CodeCarbon gera automaticamente arquivos com:
- Tempo de execução
- Energia consumida
- Emissões estimadas de CO₂

Esses arquivos ficam, normalmente, na pasta:
```
/emissions
```

---

## 7. Boas Práticas

- Medir apenas o trecho principal do código
- Comparar diferentes soluções para o mesmo problema
- Usar os dados para melhorar sistemas e processos
- Documentar o impacto ambiental em projetos de TI

---

## 8. Conclusão

O CodeCarbon é uma ferramenta simples e eficaz para aplicar os conceitos de **TI Verde** na prática.
Ele mostra que escrever códigos mais eficientes melhora o desempenho e também ajuda o meio ambiente.
