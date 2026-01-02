# Concatenate Function

**Concatenate Function to Limit Characters in Message Token Values**

If you need to limit the length of message tokens (for example, when the store name is too long), and you have added Store.Name to your message template, it will be replaced with the full store name.
To shorten the store name, you can use the plugin’s concatenate function, which limits message token characters to a defined length.

For example, {%Store.Name%[10..]} will now return “your store..” and {%Store.Name%[10]} will now return “your store” respectively.

[← Previous](customMessageTokens.md) | [Next →](History.md)