# escola
Atividade Escola Mongoose

C:\Users\fatec258>curl -X POST http://localhost:3001/professor -H "Content-Type: application/json" -d "{\"nome\": \"Henrique Louro\", \"email\": \"henrique.louro@fatec.sp.gov.br\", \"cpf\": \"07494812857\"}"
{"nome":"Henrique Louro","email":"henrique.louro@fatec.sp.gov.br","cpf":"07494812857","_id":"6838ee7bdd5afac8f912f85c","__v":0}

C:\Users\fatec258>curl -X POST http://localhost:3001/professor -H "Content-Type: application/json" -d "{\"nome\": \"Carlos Silva\", \"email\": \"carlos.silva@fatec.sp.gov.br\", \"cpf\": \" 63479695051\"}"
{"nome":"Carlos Silva","email":"carlos.silva@fatec.sp.gov.br","cpf":"63479695051","_id":"6838f229dd5afac8f912f85e","__v":0}

C:\Users\fatec258>curl -X POST http://localhost:3001/professor -H "Content-Type: application/json" -d "{\"nome\": \"Odete Roitman\", \"email\": \"odete.roitman@fatec.sp.gov.br\", \"cpf\": \" 32082128016\"}"
{"nome":"Odete Roitman","email":"odete.roitman@fatec.sp.gov.br","cpf":"32082128016","_id":"6838f262dd5afac8f912f860","__v":0}

C:\Users\fatec258>curl -X POST http://localhost:3001/professor -H "Content-Type: application/json" -d "{\"nome\": \"Henrique Louro\", \"email\": \"henrique.louro@fatec.sp.gov.br\", \"cpf\": \"07494812857\"}"
{"message":"CPF ou e-Mail já em uso"}

C:\Users\fatec258>curl -X POST http://localhost:3000/professor -H "Content-Type: application/json" -d "{\"nome\": \"Henrique Louro\", \"email\": \"henrique.louro@fatec.sp.gov.br\", \"cpf\": \"12345678910\"}"
{"message":"12345678910 não é um CPF válido"}

C:\Users\fatec258>curl -X POST http://localhost:3000/professor -H "Content-Type: application/json" -d "{\"nome\": \"Henrique Louro\", \"email\": \"henrique.louro@fatec\", \"cpf\": \"12345678910\"}"
{"message":"henrique.louro@fatec não é um formato de e-mail válido"}

C:\Users\fatec258>curl -X GET http://localhost:3000/professor
[{"_id":"6838ee7bdd5afac8f912f85c","nome":"Henrique Louro","email":"henrique.louro@fatec.sp.gov.br","cpf":"07494812857","__v":0},{"_id":"6838f229dd5afac8f912f85e","nome":"Carlos Silva","email":"carlos.silva@fatec.sp.gov.br","cpf":"63479695051","__v":0},{"_id":"6838f262dd5afac8f912f860","nome":"Odete Roitman","email":"odete.roitman@fatec.sp.gov.br","cpf":"32082128016","__v":0}]

C:\Users\fatec258>curl -X PUT http://localhost:3000/professor -H "Content-Type: application/json" -d "{\"id\":\"6838f262dd5afac8f912f860\",\"nome\": \"Odetinha Roitman\", \"email\": \"odetinha.roitman@fatec.sp.gov.br\", \"cpf\": \" 32082128016\"}"
{"_id":"6838f262dd5afac8f912f860","nome":"Odetinha Roitman","email":"odetinha.roitman@fatec.sp.gov.br","cpf":"32082128016","__v":0}

C:\Users\fatec258>curl -X DELETE http://localhost:3000/professor -H "Content-Type: application/json" -d "{\"id\":\"6838f262dd5afac8f912f860\"}"
{"message":"Professor excluído com sucesso"}

C:\Users\fatec258>curl -X GET http://localhost:3000/professor
[{"_id":"6838ee7bdd5afac8f912f85c","nome":"Henrique Louro","email":"henrique.louro@fatec.sp.gov.br","cpf":"07494812857","__v":0},{"_id":"6838f229dd5afac8f912f85e","nome":"Carlos Silva","email":"carlos.silva@fatec.sp.gov.br","cpf":"63479695051","__v":0}]

C:\Users\fatec258>curl -X POST http://localhost:3000/disciplina -H "Content-Type: application/json" -d "{\"descricao\": \"Técnicas de Programação II\"}"
{"descricao":"Técnicas de Programação II","_id":"6838f49fb5936f31979d7975","__v":0}

C:\Users\fatec258>curl -X POST http://localhost:3000/disciplina -H "Content-Type: application/json" -d "{\"descricao\": \"Lógica de Programação\"}"
{"descricao":"Lógica de Programação","_id":"6838f4c2b5936f31979d7977","__v":0}

C:\Users\fatec258>curl -X GET http://localhost:3000/disciplina
[{"_id":"6838f4c2b5936f31979d7977","descricao":"Lógica de Programação","__v":0},{"_id":"6838f49fb5936f31979d7975","descricao":"Técnicas de Programação II","__v":0}]

C:\Users\fatec258>curl -X POST http://localhost:3000/professor_has_disciplina -H "Content-Type: application/json" -d "{\"professor\": \"6838ee7bdd5afac8f912f85c\", \"disciplina\": \"6838f49fb5936f31979d7975\"}"
{"professor":"6838ee7bdd5afac8f912f85c","disciplina":"6838f49fb5936f31979d7975","_id":"6838f596b5936f31979d797a","__v":0}

C:\Users\fatec258>curl -X POST http://localhost:3000/professor_has_disciplina -H "Content-Type: application/json" -d "{\"professor\": \"6838f229dd5afac8f912f85e\", \"disciplina\": \"6838f4c2b5936f31979d7977\"}"
{"professor":"6838f229dd5afac8f912f85e","disciplina":"6838f4c2b5936f31979d7977","_id":"6838f5d3b5936f31979d797e","__v":0}

C:\Users\fatec258>curl -X POST http://localhost:3000/professor_has_disciplina -H "Content-Type: application/json" -d "{\"professor\": \"6838f229dd5afac8f912f85e\", \"disciplina\": \"6838f4c2b5936f31979d7977\"}"

C:\Users\fatec258>
