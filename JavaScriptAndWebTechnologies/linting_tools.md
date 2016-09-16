# Linting Tools

**ESLint**


ESLint is the most recent out of the four. It was designed to be easily extensible, comes with a large number of custom rules, and it’s easy to install more in the form of plugins. It gives concise output, but includes the rule name by default so you always know which rules are causing the error messages.

ESLint documentation can be a bit hit or miss. The rules list is easy to follow and is grouped into logical categories, but the configuration instructions are a little confusing in places. It does, however, offer links to editor integration, plugins and examples all in a single location


### Verdict 1

My choice of these four is **ESLint**. JSLint is strict and not configurable, whereas JSHint is lacking the extension mechanism. JSCS is a good choice if you only want to check coding style, but ESLint does that and it checks your code for bugs and other problems as well.

### Verdict 2

**JSHint** is strong second choice. If you don’t need the advanced features of ESLint, JSHint catches a good number of issues once properly configured. JSCS, with its huge number of available rules, is a top pick if you don’t need anything other than coding style checks (indentation, braces, etc.).

### verdict 3

I’m *hesitant to recommend JSLint at all*. The other tools do the same things, but don’t force any specific rules on the user. The only exception here is if you happen to agree with all the rules it enforces, in which case it might well be worth looking into.