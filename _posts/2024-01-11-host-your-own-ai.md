---
title: Host your own AI
author: cr
date: 2024-01-11 18:00:00 +0800
categories: [Tutorial, AI]
tags: [ai, self-hosted]
published: true
---

## Einleitung
In diesem Blogpost möchte ich Ihnen zeigen, wie Sie eine KI in Ihrer <b>Firma</b> oder <b>privat</b> nutzen könnnen, ohne auf Services Dritter zurückgreifen zu müssen. Dazu werde ich Ihnen anhand eines Beispiel-Projektes zeigen, wie ein Einsatz aussehen könnte. Das Tool, das wir hierzu verwenden heißt [Ollama]("https://ollama.ai/").

Zu Beginn sollten wir jedoch erst einmal klären, aus was eine KI eigentlich besteht. 
Eine KI besteht aus zwei Teilen: dem Modell und den Daten. Das Modell (auch bekannt als LLM) ist eine mathematische Funktion, die aus den Daten gelernt hat. Das Modell kann dann auf neue Daten angewendet werden.

## Ollama - Was ist das?
Wir benutzen das OpenSource Tool [Ollama]("https://ollama.ai/") um unsere KI zu hosten. Ollama ist ein Tool, das es uns ermöglicht, unsere KI auf einem eigenen Server, aber auch lokal am eigenen PC zu hosten. Dies inkludiert, dass keine Daten an Dritte weitergegeben werden. Das Tool funktioniert derzeit nur unter Linux und MacOS. Eine Windows Version ist jedoch in finaler Arbeit und wird demnächst noch kommen.

## Ollama - Installation
Das Tool zu installieren ist sehr einfach.
Für MacOS:
-> Einfach die .zip Datei herunterladen und die darin enthaltene Datei installieren.

Für Linux:
-> Folgenden Befehl ausführen
```
curl https://ollama.ai/install.sh | sh
```


## Ollama - Erste Schritte
Nachdem wir das Tool installiert haben, können wir es auch schon starten. Dazu müssen wir einfach nur den Befehl "ollama run [modelname]" in der Konsole ausführen. 
Eine Liste aller verfügbaren Modelle finden Sie [hier]("https://ollama.ai/library").

In unserem Beispiel nehmen wir das von Meta (ehemals Facebook) entwickelte Modell "llama2".
>ACHTUNG: Das Modell hat keine Apache 2.0 Lizenz und darf daher nicht kommerziell genutzt werden. Daher grundlegend immer die Lizenz des Modells prüfen.
{: .prompt-tip }
```
ollama run llama2
```


## KI erfolgreich nutzen
Nachdem wir das Modell gestartet haben, können wir es auch schon nutzen. Dazu müssen wir nur noch die IP-Adresse des Servers herausfinden.

Hier ein Beispiel, wie Sie ihre KI nutzen können
```
curl http://localhost:11434/api/generate -d '{
  "model": "llama2",
  "prompt":"Was ist eine Erdbeere?"
}'
```
<br>
<br>
<br>

# Und das wars auch schon! 🚀
Sie können nun Ihre KI nutzen. Viel Spaß damit!
Wenn Sie Fragen haben, können Sie mich gerne kontaktieren. Ich werde in naher Zukunft noch ein Tutorial veröffentlichen, indem es darum geht, wie Sie Ihre eigene KI in Kombination mit ihren Geschäftsdaten nutzen können.