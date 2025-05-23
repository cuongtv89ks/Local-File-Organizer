# Local File Organizer: AI File Management Run Entirely on Your Device, Privacy Assured

Tired of digital clutter? Overwhelmed by disorganized files scattered across your computer? Let AI do the heavy lifting! The Local File Organizer is your personal organizing assistant, using cutting-edge AI to bring order to your file chaos - all while respecting your privacy.

## How It Works 💡

Before:

```
/Users/Local-File-Organizer/sample_data
├── 1.md
├── 1.xlsx
├── 12222_777.docx
├── IMG_0967.PNG
├── c8fed35720671596882b0c6a2ad9586d.gif
├── go_bruin.pptx
├── logo.png
├── output.wav
├── paper_1col.pdf
├── sub_dir1
│   ├── 1111_63.csv
│   └── animal.jpg
├── sub_dir2
│   └── BS.txt
├── text_files
│   └── ccc.md
└── videoplayback.mp4
```

After:

```
/Users/Local-File-Organizer/organized_folder
├── excel_training
│   ├── outline_five_day.md
│   └── outline_five_day.xlsx
├── mathematics
│   └── present_fundamental_arithmetic.docx
├── string_theory
│   └── detailed_introduction_string.pdf
├── data_trend
│   └── presentation_explores_several.pptx
├── truck
│   └── present_list_ford.csv
├── travel_experience
│   └── chicago_consistently_ranked.md
├── banking_record
│   └── present_account_activity.txt
├── portrait
│   └── could_generate.gif
├── technology_brand
│   └── detailed_sent_google.png
├── storage_apps
│   └── detailed_overall_view.PNG
├── marine_life
│   └── detailed_overall_impression.jpg
├── tax_reform
│   └── corporate_tax_revisions_digital_businesses.wav
└── agent_development
    └── google_cloud_agent_development_hackathon.mp4
```

## Updates 🚀
**[2025/05] v0.0.3**:
* Major Backend Change: Switched AI inference from Nexa SDK to gemma3 and openai-whisper for local LLM/VLM processing. 
* Enhanced Text Processing: Integrated MarkItDown for robust conversion of various text file types (DOCX, PDF, PPTX, etc.) to Markdown before AI analysis. 
* Audio File Support: Added processing for audio files using Whisper for transcription and Gemma3:4b for metadata generation and image to text generation. 
* Video File Support: Added processing for video files using ffmpeg to extract audio, Whisper for transcription, and Ollama for metadata generation.
- Added file support: .md, .excel, .ppt, and .csv .txt, .docx, .doc, .pdf, .md, .xls, .xlsx, .ppt, .pptx, .csv, .mp3, .wav, .m4a, .flac, .aac, .ogg, .mp4, .mov, .avi, .mkv, .flv, .wmv.

**[2024/09] v0.0.2**:
Original from https://github.com/QiuYannnn/Local-File-Organizer.git
* Featured by [Nexa Gallery](https://nexaai.com/gallery) and [Nexa SDK Cookbook](https://github.com/NexaAI/nexa-sdk/tree/main/examples)!
* Dry Run Mode: check sorting results before committing changes
* Silent Mode: save all logs to a txt file for quieter operation
* Added file support:  `.md`, .`excel`, `.ppt`, and `.csv` 
* Three sorting options: by content, by date, and by type
* The default text model is now [Llama3.2 3B](https://nexaai.com/meta/Llama3.2-3B-Instruct/gguf-q3_K_M/file)
* Improved CLI interaction experience
* Added real-time progress bar for file analysis

Please update the project by deleting the original project folder and reinstalling the requirements. Refer to the installation guide from Step 4.


## Roadmap 📅

- [ ] Copilot Mode: chat with AI to tell AI how you want to sort the file (ie. read and rename all the PDFs)
- [ ] Change models with CLI 
- [x] ebook format support
- [x] audio file support
- [x] video file support
- [ ] Implement best practices like Johnny Decimal
- [x] Check file duplication and more for pre-processing sort file-> using https://github.com/tfeldmann/organize 
- [ ] Dockerfile for easier installation

## Prerequisites 💻

- **Operating System:** Compatible with Windows, macOS, and Linux.
- **Python Version:** Python 3.12
- **Conda:** Anaconda or Miniconda installed.
- **Git:** For cloning the repository (or you can download the code as a ZIP file).
- **Ollama**: Installed and running on your system. Download from ollama.com. 
- **markitdown**: for converting some file types. Install from pandoc.org.
- **ffmpeg**: Required for extracting audio from video files. Install from ffmpeg.org.

## Installation 🛠

### 1. Install Python

Before installing the Local File Organizer, make sure you have Python installed on your system. We recommend using Python 3.12 or later.

You can download Python from [the official website]((https://www.python.org/downloads/)).

Follow the installation instructions for your operating system.

### 2. Clone the Repository

Clone this repository to your local machine using Git:

```zsh
git clone https://github.com/cuongtv89ks/Local-File-Organizer
```


Or download the repository as a ZIP file and extract it to your desired location.

### 3. Set Up the Python Environment

Create a new Conda environment named `local_file_organizer` with Python 3.12:

```zsh
conda create --name local_file_organizer python=3.12
```

Activate the environment:

```zsh
conda activate local_file_organizer
```
### 4. Install Dependencies 

1. Ensure you are in the project directory:
   ```zsh
   cd path/to/Local-File-Organizer
   ```
   Replace `path/to/Local-File-Organizer` with the actual path where you cloned or extracted the project.

2. Install the required dependencies:
   ```zsh
   pip install -r requirements.txt
   ```

   ```zsh
   # on Ubuntu or Debian
  sudo apt update && sudo apt install ffmpeg

    # on Arch Linux
    sudo pacman -S ffmpeg

    # on MacOS using Homebrew (https://brew.sh/)
    brew install ffmpeg

    # on Windows using Chocolatey (https://chocolatey.org/)
    choco install ffmpeg

    # on Windows using Scoop (https://scoop.sh/)
    scoop install ffmpeg
   ```

With the environment activated and dependencies installed, run the script using:

### 5. Running the Script🎉
```zsh
python main.py
```

## Notes
- **Processing Time:**
  - Processing may take time depending on the number and size of files.
  - The script uses multiprocessing to improve performance.

- **Customizing Prompts:**
  - You can adjust prompts in `data_processing.py` to change how metadata is generated.

## License

This project is dual-licensed under the MIT License and Apache 2.0 License. You may choose which license you prefer to use for this project.

- See the [MIT License](LICENSE-MIT) for more details.