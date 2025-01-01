# Tailwind CSS: Styles not applied from custom component in node_modules
This repository demonstrates a common issue encountered when using Tailwind CSS with custom components located within the `node_modules` directory. The problem arises when Tailwind's `content` configuration fails to include the necessary paths for the custom components, preventing the styles from being applied.

## Bug Description
The primary issue lies in the incorrect configuration of the `content` option within the `tailwind.config.js` file.  If this configuration does not explicitly include the directory containing your custom component, Tailwind won't process the styles within those components.

## Solution
The solution involves ensuring that the `content` array in your `tailwind.config.js` includes the paths to your custom components within `node_modules`. 

This requires specifying the complete path to the directory containing the component files.  Relative paths from the project root are not always sufficient when dealing with components within `node_modules`.