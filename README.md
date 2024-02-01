# Translating a medical report into fixed categories using GPT-3.5

key libraries:  
pytesseract: [https://github.com/tesseract-ocr/tesseract](https://pypi.org/project/pytesseract/)  
openai: https://pypi.org/project/openai/ 

## image used as pseudo medical report:
[<img src="dummy_data\\Bsp_Arztbrief.jpg">](https://de.wikipedia.org/wiki/Arztbrief#/media/Datei:Arztbrief.jpg)

text is extracted from the image (.jpg) using pytersseract

after extracting text from the image (.jpg), gpt-3.5 is implemented to extract information based on fixed categories 

## fixed categories used
kategorien = [
    "Name des behandelnden Arztes",
    "Name des angesprochenen Arztes",
    "Name des Patienten",
    "Diagnose",
    "Therapie",
    "Behandlungsverlauf",
    "Ergebnis"
]

please note, that the categories need adjustement based on the specific infromation of interest  

for the exact procedure, please refer to the [code](https://github.com/georg-popp/bihagent/blob/main/dummy_code/smart_letter.ipynb)

## output of categorization using gpt-3.5 

***Name des behandelnden Arztes:** Prof. O. ne
**Name des angesprochenen Arztes:** Dr. me or  
**Name des Patienten:** N/A (nicht angegeben)  
**Diagnose:** Hochgradig kombiniertes Aortenvitium mit Druckgradient von 110 mmHG, Dekompensation. Supravalvulire Aortenstenose  
**Therapie:** Implantation einer St. Jude Medical Gr. 25 in Aortenposition, Patcherweiterung der Aorta ascendens supravalvular  
**Behandlungsverlauf:** Erfolgreicher herzchirurgischer Eingriff am 26.10.49, Patient befindet sich auf der Intensivstation, extubiert, Sinusrhythmus vorhanden, neuimplantierte Klappe arbeitet einwandfrei, keine Hinweise auf Dysfunktion, keine Substanzen notwendig  
**Ergebnis:** Komplikationsloser Verlauf erwartet, weitere Berichte folgen bei Verlegung*

please note, that the content of each category is *guessed* by gpt-3.5 without any further adjustments  

please note, that the exact results might not be restored using the same code. For more information on chatGPT please click [here](https://towardsdatascience.com/how-chatgpt-works-the-models-behind-the-bot-1ce5fca96286)

## optimization based on the initial results
- **Data Cleaning**: ensure input data is correct
- **Model Fine-tuning**: train model on specific task or dataset 
- **Advanced Categorization**: add categories or subcategories for detailed classification
- **Use of Context**: provide context information
- **Human Review**: human review of results to identify errors and areas for improvement

tbd. 
