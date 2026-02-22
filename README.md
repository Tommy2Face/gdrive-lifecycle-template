# Google Drive Lifecycle Template

Ready-to-use folder structure template for Google Drive, based on the BH Lifecycle Matrix v4.1. Provides standardized phase-based folders with `_INDEX.md` files for AI-searchable document management across Dutch real estate SPV entities.

## Structure

```
00.2_Entity_Administration/
01_PIPELINE/
02_ACQUISITION/
03_DEVELOPMENT/
04_REALIZATION/
05_OPERATIONS/
06_EXIT/
08_FINANCING/
```

Each phase contains entity-level subfolders (e.g., `BH_Bakkers_Hommen_Group/`) with `_INDEX.md` files listing expected document categories.

## Usage

Copy the template into Google Drive and rename the entity folders to match your project/SPV:

```bash
# Or generate custom structures programmatically:
# See lifecycle-matrix-v4.1-deploy for the generate_structure.py script
python3 generate_structure.py --type spv --code ME1 --name "MaxEuwelaan 1" --dry-run
```

## Context

Part of the three-tier data architecture for Bakkers|Hommen Group:

| Tier | Platform | Role |
|------|----------|------|
| 1 | SharePoint | Source of truth — finals, signed docs |
| 2 | **Google Drive** | AI-facing collaboration — working drafts, AI indexes |
| 3 | Dropbox | Confidential vault — management-only |

This template is for Tier 2 (Google Drive).

## License

Proprietary — Bakkers|Hommen Group
