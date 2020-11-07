# Mappings

`fhossyl-mappings` is a repository dedicated to provide all blocks, sounds, effects, recipes, 
particles and items with their respective name for each platform.

# Structure

Particles, items, recipes, blocks and effects can be different in the Java Edition and Bedrock 
Edition platforms; keeping this in mind, we check if `fhossyl-mapping` contains the element we want,
otherwise we take the default element (in which would be the one that comes from the Java Edition).

Some blocks may have the same identification, but some information (like hardness, type of tool, etc.)
may be different, so we must map it too.

```yaml
# Block mapping structure
blocks:
  polished_diorite: # Java edition identifier
    bedrock_identifier: stone
    block_hardness: 1.5
    drop_with_hand: false
    tool_type: pickaxe
    bedrock_states:
     stone_type: diorite_smooth

# Item mapping structure
items:
  stone: # Java edition identifier
    bedrock_identifier: 1
    bedrock_data: 0
    is_block: true

# Recipe mapping structure
recipes:
  leather_armor: # Java edition identifier
    1: [leather, air, leather]
    2: [leather, leather, leather]
    3: [leather, leather, leather]
  stone_sword:
    1: [air, cobblestone, air]
    2: [air, cobblestone, air]
    3: [air, stick, air]
```