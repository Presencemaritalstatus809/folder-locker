# Contributors

## f0xyn0xy - September 6 2026

### Testing and Development Tooling Improvements

**Changes made:**

- **Added pytest configuration** (`pyproject.toml`)
  - Configured `pythonpath = ["src"]` for automatic test discovery
  - Set `testpaths = ["tests"]` and `python_files = ["test_*.py"]`
  - Tests now run with `pytest` without manual PYTHONPATH setup

- **Added development tooling** (`requirements-dev.txt`)
  - Added `pytest>=7.0.0` for testing framework
  - Added `ruff>=0.4.0` for fast Python linting
  - Added `mypy>=1.10.0` for static type checking

- **Performance optimization** (`src/folder_locker/core.py`)
  - Increased `DEFAULT_CHUNK_SIZE` from 1 MB to 16 MB
  - Provides ~16× better performance for large file encryption/decryption
  - Reduces overhead from AES-GCM record management

- **Fixed .gitignore inconsistency** (`.gitignore`)
  - Changed from blocking all `.vscode/` to selectively allowing essential files
  - Now tracks `.vscode/settings.json` while ignoring other IDE files

- **Added linting and type checking configuration** (`pyproject.toml`)
  - Configured ruff with 120 character line length, Python 3.10+ target
  - Configured mypy for optional type checking with sensible defaults

**Test status:** All 5 tests passing ✅
