# VisitaSaúde

App Flutter de apoio a **agentes comunitários de saúde (ACS)** em visitas domiciliares.
Disciplina: Programação para Dispositivos Móveis – USCS | Prof. Me. Raphael Lopes de Souza | Entrega: 02/12/2026

## Problema e justificativa
ACS fazem dezenas de visitas por dia, conferindo endereços, enfrentando o clima e consultando
informações de medicamentos, em geral em papel, WhatsApp ou de memória. O app reúne essas consultas
em um só lugar, no celular. Não é app recreativo: apoia a rotina profissional na área da saúde.

**Pesquisa de campo** (15 agentes comunitários de saúde; tabulação em `pesquisa_campo_visitasaude.xlsx`):
- Média de **12,8 visitas/dia** (mín. 7, máx. 20); **100%** usam celular no trabalho.
- **33%** registram as visitas em papel, **27%** por WhatsApp, **27%** em sistema e **13%** de memória.
- Dificuldade média para localizar endereços: **3,6/5**; consulta a medicamentos: **3,6/5**.
- **87%** relatam que o clima atrapalha a rotina.
- Utilidade percebida do app: **4,6/5**.
- Funcionalidades citadas: consulta de CEP/endereço, clima e previsão de chuva, medicamentos, checklist de visitas.

Os resultados sustentam as 3 telas do protótipo (endereço, clima e medicamentos).

## Protótipo (baixa fidelidade) – 3 telas com consumo de API
| Tela | API | Função |
|---|---|---|
| Endereço | ViaCEP | Confirma logradouro/bairro/cidade pelo CEP |
| Clima | Open-Meteo | Temperatura, umidade, previsão de chuva + alerta de calor (local por geocoding) |
| Medicamento | openFDA | Indicações por nome genérico (PT→EN para nomes comuns) + aviso de confirmação em fonte oficial |

Wireframes: ver `Wireframes_do_app_VisitaSaude.png` (3 telas com barra de navegação inferior). Copie o PNG para a pasta `docs/` do repositório.

## Como rodar
```
flutter create .      # gera android/ios/etc. (rodar na pasta do projeto)
flutter pub get
flutter run
```
Android: adicione `<uses-permission android:name="android.permission.INTERNET"/>` em `android/app/src/main/AndroidManifest.xml` se necessário.

## Questionário aplicado
Profissão, visitas/dia, experiência, registro atual, dificuldade com endereços (1-5), consulta a medicamentos (1-5), clima atrapalha?, usa celular no trabalho?, utilidade do app (1-5) e funcionalidade desejada. Dados em `pesquisa_campo_visitasaude.xlsx` (aba Respostas) e resumo com gráficos (aba Resumo).

## Entrega
Repositório **público** no GitHub; enviar só o link no Google Classroom até 02/12/2026.
Integrantes (máx. 5): ______
