from googletrans import Translator, LANGUAGES

def translate_text(text, target_language):
    translator = Translator()
    translated = translator.translate(text, dest=target_language)
    return translated.text

def main():
    print("Welcome to the English to Any Language Translator!")
    
    # Display available languages
    print("Available languages:")
    for lang_code, lang_name in LANGUAGES.items():
        print(f"{lang_code}: {lang_name}")

    # Get user input
    text_to_translate = input("Enter the text you want to translate: ")
    target_language = input("Enter the language code you want to translate to (e.g., 'fr' for French): ")

    # Perform translation
    try:
        translated_text = translate_text(text_to_translate, target_language)
        print(f"Translated text: {translated_text}")
    except Exception as e:
        print(f"An error occurred: {e}")

if __name__ == "__main__":
    main()
