# Model Creation

**For Internal Developer Use Only**

We recognize that questions may arise about creating addon mods, so we've documented this information for reference.

## Bedrock Model Loading

All console, shell, interior door models, and some blocks utilize bedrock geometry for easier updates. Instead of relying on an external mod, we use our in-house solution

### Can I Use All Bedrock Geometry Features?

Not entirely. Below are the currently known limitations:

- **No Part Rotations**: Rotations must be implemented using rotated groups instead.
- **Decimal Parts**: These are supported.
- **UV Rotating**: This feature doesn’t work. To achieve the same effect, manually adjust the U and V coordinates by swapping their positive/negative values.
- **Part Inflation**: 100% fine!

