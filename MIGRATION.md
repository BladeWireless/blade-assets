# Asset Migration Guide

## Overview

This repository has been renamed from `blade-assets` to `raku-assets` as part of the Raku SDK rebrand initiative. This guide helps dependent repositories update their references to continue accessing assets correctly.

## Repository Rename

- **Old Name**: `blade-assets`
- **New Name**: `raku-assets`
- **Organization**: BladeWireless (unchanged)
- **Effective Date**: 2025-11-03

## What Changed

### Repository URL

The repository URL has been updated:

- **Old URL**: `https://github.com/BladeWireless/blade-assets`
- **New URL**: `https://github.com/BladeWireless/raku-assets`

GitHub automatically redirects the old URL to the new one, but we recommend updating references for long-term maintainability.

### Asset Files

Asset file names remain unchanged:
- `demos/Space_Battleship_Defense.zip`
- `demos/Space_Battleship_Defense.mp4`

Asset content has been updated to reflect Raku SDK branding (completed 2025-10-31).

### Documentation

- `README_assets.md` has been renamed to `README.md` (standard convention)
- All documentation now references Raku SDK instead of legacy platform names

## Migration Steps

### Step 1: Update Repository References

If your project references this repository, update the URLs:

**Git Submodules:**
```bash
# Update .gitmodules file
sed -i 's|BladeWireless/blade-assets|BladeWireless/raku-assets|g' .gitmodules

# Sync the changes
git submodule sync
git add .gitmodules
git commit -m "Update blade-assets reference to raku-assets"
```

**Direct Git Clones:**
```bash
# Update your clone's remote URL
git remote set-url origin https://github.com/BladeWireless/raku-assets.git
```

### Step 2: Update Asset Download URLs

Update any scripts or documentation that download assets:

**Before:**
```bash
curl -L -O https://raw.githubusercontent.com/BladeWireless/blade-assets/main/demos/Space_Battleship_Defense.zip
```

**After:**
```bash
curl -L -O https://raw.githubusercontent.com/BladeWireless/raku-assets/main/demos/Space_Battleship_Defense.zip
```

### Step 3: Update Documentation References

Search your documentation for references to `blade-assets` and update them to `raku-assets`:

```bash
# Find all references (example)
grep -r "blade-assets" docs/ README.md

# Update references
sed -i 's|blade-assets|raku-assets|g' docs/*.md README.md
```

### Step 4: Update CI/CD Pipelines

If your CI/CD pipelines reference this repository, update the URLs:

**GitHub Actions:**
```yaml
# Before
- uses: actions/checkout@v3
  with:
    repository: BladeWireless/blade-assets
    
# After
- uses: actions/checkout@v3
  with:
    repository: BladeWireless/raku-assets
```

**Scripts:**
```bash
# Update any shell scripts that clone or reference the repository
ASSETS_REPO="https://github.com/BladeWireless/raku-assets.git"
```

## Asset Compatibility

### No Breaking Changes

- All asset files remain at the same paths within the repository
- Asset file names are unchanged
- Asset content is backward-compatible with Raku devices
- GitHub provides automatic redirects from old URLs to new URLs

### What You Don't Need to Change

You do **not** need to update:
- Asset file paths within the repository
- Asset integration code in your Unity projects
- Asset processing scripts (unless they reference the repository name)

## Common Migration Scenarios

### Scenario 1: Direct Asset Downloads

If you download assets directly via URL, update the repository name in your URLs. The old URLs will redirect, but updating ensures future compatibility.

### Scenario 2: Git Submodule

If you use this repository as a submodule, update your `.gitmodules` file and run `git submodule sync`.

### Scenario 3: Documentation Links

Update any documentation that links to this repository to use the new name for clarity.

### Scenario 4: Build Scripts

Review and update build scripts that clone or reference this repository.

## Verification

After migration, verify your changes:

1. **Test Asset Downloads**: Ensure your scripts can download assets successfully
2. **Check Documentation**: Verify all links point to the correct repository
3. **Run CI/CD**: Confirm pipelines execute without errors
4. **Review Logs**: Look for any references to the old repository name

## Timeline

- **2025-10-31**: Asset metadata updated for Raku SDK
- **2025-11-03**: Repository renamed to `raku-assets`
- **Ongoing**: GitHub redirects from old URLs remain active indefinitely

## Support

If you encounter issues during migration:

1. Check this migration guide for common scenarios
2. Review the [README.md](./README.md) for current asset information
3. Consult the main SDK repository: https://github.com/BladeWireless/raku-sdk
4. Contact the SDK team via the main raku-sdk repository

## Checklist

Use this checklist to track your migration:

- [ ] Updated git remote URLs or submodule references
- [ ] Updated asset download URLs in scripts
- [ ] Updated documentation references
- [ ] Updated CI/CD pipeline configurations
- [ ] Tested asset downloads and integrations
- [ ] Verified all links work correctly
- [ ] Removed old repository references from codebase
- [ ] Updated team documentation and wikis

## Additional Resources

- [Raku SDK Repository](https://github.com/BladeWireless/raku-sdk)
- [Space Battleship Defense Demo Documentation](./demos/)
- [Asset Usage Guide](./README.md#usage)

---

**Note**: While GitHub provides automatic URL redirects, we strongly recommend updating all references to ensure long-term maintainability and avoid potential issues if redirect behavior changes in the future.
