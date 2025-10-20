# Testes Automatizados com Python

Este repositório reúne exemplos práticos de **automação de testes** utilizando Python e as bibliotecas **Pytest**, **Requests** e **Selenium**.  
O objetivo é demonstrar como aplicar boas práticas de testes em diferentes contextos — desde funções simples até interfaces web e APIs reais.

---

## Estrutura do Projeto

automated-tests-python/
│
├── calculadora/
│ ├── calculadora.py # Funções simples para testes unitários
│ └── test_calculadora.py # Testes unitários com Pytest
│
├── api_tests/
│ └── test_api_jsonplaceholder.py # Testes de API pública com Requests + Pytest
│
├── ui_tests/
│ └── test_google_search.py # Teste de interface com Selenium (busca no Google)
│
├── report.html # Relatório HTML gerado pelo pytest-html
│
└── requirements.txt # Dependências do projeto

---

# Tecnologias Utilizadas

| Ferramenta | Função |
|-------------|--------|
| **Python 3** | Linguagem principal |
| **Pytest** | Framework de testes |
| **Requests** | Testes de API REST |
| **Selenium WebDriver** | Automação de interface (UI) |
| **Pytest-HTML** | Geração de relatórios visuais em HTML |

---

## Instalação e Execução

## Execute todos os testes:
pytest -v

## Gere um relatório HTML interativo:
pytest --html=report.html --self-contained-html -v
Abra o relatório:

## No navegador: 
abra o arquivo report.html
Ou diretamente no Jupyter/Colab: https://colab.research.google.com/drive/1vsucgrxpLw5Fmb93r_5eGRIqQpa0aQ3Q?usp=sharing
from IPython.display import HTML
HTML(open("report.html").read())

## Exemplos de Testes

- Teste Unitário (funções simples)
def test_somar():
    assert somar(2, 3) == 5
  
- Teste de API
def test_get_posts_status_code():
    response = requests.get("https://jsonplaceholder.typicode.com/posts")
    assert response.status_code == 200
  
- Teste de Interface (UI)
def test_google_search(driver):
    driver.get("https://www.google.com")
    search_box = driver.find_element(By.NAME, "q")
    search_box.send_keys("Python Selenium")
    search_box.send_keys(Keys.RETURN)
    assert "Selenium" in driver.page_source
  
## Relatório HTML
Os resultados dos testes são gerados automaticamente com pytest-html, mostrando:
- Testes aprovados e falhos
- Tempo de execução
- Logs e detalhes técnicos
Exemplo de relatório:

## Aprendizados
- Aprendi a organizar testes unitários em Python, validar endpoints de API e automatizar interações em páginas web com Selenium.
- Geração e interpretação de relatórios interativos
- Boas práticas de QA aplicadas em Python

## Próximos Passos
- Adicionar prints automáticos em falhas de UI
- Integrar com GitHub Actions (CI/CD)
- Testar APIs com autenticação e payloads complexos

👩‍💻 Autora
Ingrid Pessoa Bighetti
💼 [LinkedIn](https://www.linkedin.com/in/ingrid-pessoa-bighetti-79849650/) | 💻 [GitHub](https://github.com/ingridbighetti)

