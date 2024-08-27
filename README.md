# Run from Git

1. Clone the repository
2. Make sure the `src/generated` folder in your project is empty.
3. Run the Gradle task `runData` and wait for it to finish.
4. Run the Gradle task `runClient` to start Minecraft in developer mode with the mod installed.

# Export Mod as Jar

1. Clone repository
2. Make sure the `src/generated` folder in your project is empty.
3. Run the Gradle task `runData` and wait for it to finish.
3. Run the Gradle task `build` and wait for it to finish.
5. The `jar` is in your project folder under `build/libs`.

# Add Custom Brushing Recipes
## Brushing Recipe
Brushing recipes are applied when a brush is right-clicked with another item in the other hand.
1. Go to `core/datagen/ModRecipeProvider`. You should find a method named `buildRecipes`.
2. Use the `BrushingRecipeBuilder` class to make a recipe.
3. Ensure that you call the `.build` method, and make sure that no two recipes have the same name. The recipe is normally named after the output item.
4. Delete the generated folder (or use the Gradle task `clean`) and `runData` again.

## Water Brushing (Washing) Recipe
Water Brushing recipes are applied when the player right-clicks on water when holding an item or right clicks while holding an item with a water bottle in the other hand.
The process to add a new Water Brushing recipe is the same as for adding a normal Brushing recipe, with one difference: at step 2, use the `WaterWashingRecipeBuilder` instead.
