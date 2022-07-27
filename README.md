# GRUMPHP
## Installation
```bash
  composer require --dev creatuity/magento-quality-tools-configuration
 ```

Add following to your composer.json

```bash
  "extra": {
    "grumphp": {
            "config-default-path": "vendor/magento-quality-tools-configuration/grumphp.yml"
        }
  }
```

## Usage
- Branch names - we allow only to use branch names like `feature|bugfix|hoftix/XXX-123-short-description` for task branches and `release/x.x.x` for release branches
- Commit message - Your commit message **MUST** contain JIRA task number and short description - `[XXX-123] Add feature to alert admin for new user registration`
- When you want to commit your changes, type 
```bash
./vendor/bin/grumphp git:pre-commit
```
to run tasks defined in `grumphp.yml` **only** on the code from the commit.
## Known Issues
- If you're getting an error like this one : 
```bash
Warning: class_implements(): Class Vendor\Module\Setup\Patch\Data\ExamplePatch does not exist and could not be loaded in /dev/tests/static/framework/Magento/CodeMessDetector/Rule/Design/AllPurposeAction.php on line 35
```
check this issue on the Github https://github.com/magento/magento2/issues/33430

## Roadmap
- Add testsuite for CI pipeline.
