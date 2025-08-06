  # 🚨 DEPRECATED: Liquibase GitHub Actions

  > **⚠️ IMPORTANT**: These individual GitHub Actions are **deprecated** and will not be updated for Liquibase 5.x and beyond.

  ## 🔄 Migrate to the Official Action

  **Use the new unified Liquibase action instead:**

  ```yaml
  - uses: liquibase/setup-liquibase@v1
    with:
      version: '4.32.0'  # Requires 4.32.0 or higher
      edition: 'oss'
  - run: liquibase update --changelog-file=changelog.xml

  Migration Examples

  ❌ Old Approach (Deprecated):
  - uses: liquibase-github-actions/update@v4.33.0
    with:
      changelogFile: 'changelog.xml'
      url: 'jdbc:h2:mem:test'

  ✅ New Approach (Recommended):
  - uses: liquibase/setup-liquibase@v1
    with:
      version: '4.33.0'
      edition: 'oss'
  - run: liquibase update --changelog-file=changelog.xml --url=jdbc:h2:mem:test

  📋 Migration Steps

  1. Check your Liquibase version - Ensure you're using 4.32.0 or higher
  2. If using older version - Update to 4.32.0+ first using current micro actions
  3. Then migrate - Switch to liquibase/setup-liquibase@v1

  🕐 Support Timeline

  - Liquibase 4.x: ✅ Continued support for existing micro actions
  - Liquibase 5.x: ❌ No updates - Use setup-liquibase@v1 only

  🆘 Need Help?

  - **New Action Documentation**: [https://github.com/liquibase/setup-liquibase](https://github.com/liquibase/setup-liquibase)
  - **Migration Guide**: See examples above
  - **Issues**: Report problems at [https://github.com/liquibase/setup-liquibase/issues](https://github.com/liquibase/setup-liquibase/issues)
