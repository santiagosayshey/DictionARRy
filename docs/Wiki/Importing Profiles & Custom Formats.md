Once you've decided which profiles suit you best, the process of importing the necessary custom formats and quality profiles is straightforward.

# Profilarr

Profilarr is a Python-based tool designed to add import/export functionality to the \*arr suite. It offers a user-friendly way to export and import custom formats and quality profiles between Radarr and Sonarr installations.

## ⚠️ Before Continuing

- **This tool will overwrite any custom formats in your \*arr installation that have the same name.**
- **Custom Formats MUST be imported before syncing any premade profile.**
- **Always back up your Radarr and Sonarr configurations before using Profilarr to avoid unintended data loss.** (Seriously, do it. Even I've lost data to this tool because I forgot to back up my configs.)

## 🛠️ Installation

### Prerequisites

- Python 3.x installed. You can download it from [python.org](https://www.python.org/downloads/).
- Radarr / Sonarr

### 📦 Dependencies

- `requests` (Install using `pip install requests`)

### Initial Setup

1. Download the latest Profilarr package from the [release section](https://github.com/santiagosayshey/Profilarr/releases)
2. Extract its contents into a folder.
3. Open the `config.json` file in a text editor.
   - Add your Radarr / Sonarr API key and modify the base URL as necessary.
   - If importing / exporting, only change the master installation's API key and base URL.
   - If syncing, add the API keys and base URLs of all instances you want to sync.
   - The master install will be the one that all other instances sync to.
4. Save the changes.

## 🚀 Usage

### Exporting

1. Run `python exportarr.py` in your command line interface.
2. Follow the on-screen prompts to select the app (Radarr or Sonarr) and the data (Custom Formats or Quality Profiles) you want to export.
3. Exported data will be saved in respective directories within the tool's folder.

### Importing

1. Run `python importarr.py` in your command line interface.
2. Follow the on-screen prompts to select the app and the data you want to import.
3. Choose the specific file for Custom Formats or select a profile for Quality Profiles.
4. The data will be imported to your selected Radarr or Sonarr installation.

### Syncing

1. Run `python syncarr.py` in your command line interface.
2. The script will automatically export data from the master instance and import it to all other instances specified in `config.json`.
3. This feature is designed to manage multiple Radarr/Sonarr instances, syncing profiles and formats seamlessly.

### Radarr and Sonarr Compatibility

- Custom formats _can_ be imported and exported between Radarr and Sonarr (but might not work as expected).
- Quality profiles are not directly interchangeable between Radarr and Sonarr due to differences in quality source names. If you want to use the same profile in both apps, you will need to manually edit the profile's quality source names before importing it.

## 🌟 Upcoming Features

- **Lidarr Support:** Expand functionality to include Lidarr, allowing users to manage music quality profiles and custom formats.
- **User Interface (UI):** Development of a graphical user interface (GUI) for easier and more intuitive interaction with Profilarr. This UI will cater to users who prefer graphical over command-line interactions.
- **Automatic Updates:** Implement an auto-update mechanism for Profilarr, ensuring users always have access to the latest features, improvements, and bug fixes without manual intervention.
