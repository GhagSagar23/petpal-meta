# petpal-meta

This repository contains meta-information, configurations, documentation, and potentially infrastructure definitions related to the PetPal project ecosystem.

## Folder Structure

Below is an overview of the project's directory structure and the purpose of key folders and files.

```plaintext
petpal-meta/
├── LICENSE
├── pets
│   ├── behaviour
│   │   ├── compatiblity.json
│   │   ├── exercise.json
│   │   ├── fear_anxieties.json
│   │   ├── grooming.json
│   │   ├── markings.json
│   │   ├── temperament.json
│   │   ├── training.json
│   │   └── vaccination-steps.json
│   ├── breeds
│   │   ├── amphibian.json
│   │   ├── arachnid.json
│   │   ├── bird.json
│   │   ├── cat.json
│   │   ├── chicken.json
│   │   ├── chinchilla.json
│   │   ├── dog.json
│   │   ├── ferret.json
│   │   ├── fish.json
│   │   ├── gerbil.json
│   │   ├── guinea_pig.json
│   │   ├── hamster.json
│   │   ├── hedgehog.json
│   │   ├── horse.json
│   │   ├── insect.json
│   │   ├── lizard.json
│   │   ├── mouse.json
│   │   ├── rabbit.json
│   │   ├── rat.json
│   │   ├── reptile.json
│   │   ├── snake.json
│   │   ├── tortoise.json
│   │   └── turtle.json
│   ├── chronic_conditions.json
│   ├── coat-types.json
│   └── species.json
└── README.md
```
## Accessing Raw Data Files

The raw JSON data files within the `pets/` directory can be accessed directly via HTTP GET requests. These URLs point to the files in the `develop` branch of the repository hosted on GitHub.

### Base URL

The base host URL for accessing raw files within the `pets/` directory is:
```
https://raw.githubusercontent.com/GhagSagar23/petpal-meta/refs/heads/develop/pets
```

### Accessing General Files

To access files located directly under the `pets/` directory (like `species.json`, `coat-types.json`, `chronic_conditions.json`), append the filename to the base URL:

*   **Example (`species.json`):**
    ```
    https://raw.githubusercontent.com/GhagSagar23/petpal-meta/refs/heads/develop/pets/species.json
    ```
*   **Example (`coat-types.json`):**
    ```
    https://raw.githubusercontent.com/GhagSagar23/petpal-meta/refs/heads/develop/pets/coat-types.json
    ```

### Accessing Breed Files

To access the JSON file containing breeds for a specific species, use the following URL pattern:
```
https://raw.githubusercontent.com/GhagSagar23/petpal-meta/refs/heads/develop/pets/breeds/<species>.json
```
Replace `<species>` with the corresponding filename found within the `pets/breeds/` directory. These filenames generally correspond to the lowercase version of the species `value` found in `pets/species.json`, with spaces replaced by underscores (`_`).

*   **Example (Dog breeds):** The filename is `dog.json`.
    ```
    https://raw.githubusercontent.com/GhagSagar23/petpal-meta/refs/heads/develop/pets/breeds/dog.json
    ```
*   **Example (Cat breeds):** The filename is `cat.json`.
    ```
    https://raw.githubusercontent.com/GhagSagar23/petpal-meta/refs/heads/develop/pets/breeds/cat.json
    ```
*   **Example (Guinea Pig breeds):** The filename is `guinea_pig.json`.
    ```
    https://raw.githubusercontent.com/GhagSagar23/petpal-meta/refs/heads/develop/pets/breeds/guinea_pig.json
    ```

### Accessing Behaviour Files

Similarly, files detailing specific pet behaviours can be accessed under the `behaviour/` subdirectory:
```
https://raw.githubusercontent.com/GhagSagar23/petpal-meta/refs/heads/develop/pets/behaviour/<behaviour_topic>.json
```

*   **Example (`temperament.json`):**
    ```
    https://raw.githubusercontent.com/GhagSagar23/petpal-meta/refs/heads/develop/pets/behaviour/temperament.json
    ```
*   **Example (`exercise.json`):**
    ```
    https://raw.githubusercontent.com/GhagSagar23/petpal-meta/refs/heads/develop/pets/behaviour/exercise.json
    ```

---

**Summary:**

You can access the raw JSON files by constructing URLs starting with `https://raw.githubusercontent.com/GhagSagar23/petpal-meta/refs/heads/develop/pets/` and appending the relative path to the specific JSON file you need (e.g., `species.json`, `breeds/dog.json`, `behaviour/grooming.json`).
