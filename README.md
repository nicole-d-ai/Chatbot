# 🤖 Chatbot

**Procesamiento del Habla**

🧩 Descripción general

Este proyecto consiste en la creación de un Chatbot de tipo retrieval-based (basado en búsqueda de similitudes), que responde preguntas a partir de un dataset personalizado de preguntas y respuestas.

Se desarrollaron dos versiones del chatbot:

* 💬 Chatbot con TF-IDF y Similitud del Coseno

* 🧠 Chatbot con Embeddings preentrenados en español (spaCy)

La temática elegida fue una App de servicios que conecta clientes con profesionales (gasistas, electricistas, albañiles, diseñadores, etc.), simulando un asistente que responde consultas frecuentes de usuarios.

🧠 Conceptos principales

🔹 Chatbot TF-IDF + Cosine Similarity

* Se utilizó TfidfVectorizer (de sklearn) para convertir las preguntas en vectores numéricos.

* TF-IDF asigna más peso a las palabras clave y menos a las comunes.

* Se aplicó cosine_similarity para comparar la pregunta del usuario con las preguntas del dataset.

* El chatbot devuelve la respuesta de la pregunta más parecida.

🔹 Chatbot con Embeddings (spaCy)

* Se utilizó el modelo preentrenado en español es_core_news_md de spaCy.

* Cada pregunta se convierte en un vector semántico de 300 dimensiones, que representa el significado del texto.

* Se compara la consulta del usuario con todas las preguntas usando similitud del coseno.

* Este enfoque entiende sinónimos y reformulaciones (ej.: “gasista con matrícula” ≈ “gasista certificado”).

🧰 Librerías utilizadas

**pandas organización de datos**

**numpy manipulación de vectores y matrices**

**scikit-learn TF-IDF y similitud del coseno**

**spaCy embeddings preentrenados en español**

**es_core_news_md	modelo de lenguaje en español con vectores semánticos**

🧾 Conclusiones

* El modelo TF-IDF funciona bien con coincidencias literales (palabras exactas).

* El modelo de Embeddings logra mayor flexibilidad, entendiendo frases con distinto vocabulario.

* Incorporar un filtro por rol (cliente/profesional/general) mejora la precisión de las respuestas.

* Se evidencia que los embeddings capturan mejor el significado semántico del texto, mientras que TF-IDF capta la presencia de palabras clave.

✨ Autora

👩‍💻 Nicole Desire Ferreyra Cientifica de datos


