# Image Organization Guide

## Folder Structure
```
/images/
├── items/           # Single round items
│   ├── item_1.jpg   # KitchenAid Stand Mixer
│   ├── item_2.jpg   # iPhone 15 Pro
│   ├── item_3.jpg   # Dyson V15 Vacuum
│   └── item_X.jpg   # Additional single items
├── showcases/       # Showcase round items
│   ├── showcase_1_item_1.jpg  # Kitchen Package - Coffee Maker
│   ├── showcase_1_item_2.jpg  # Kitchen Package - Toaster Oven
│   ├── showcase_1_item_3.jpg  # Kitchen Package - Stand Mixer
│   ├── showcase_2_item_1.jpg  # Tech Bundle - Wireless Headphones
│   ├── showcase_2_item_2.jpg  # Tech Bundle - Tablet
│   └── showcase_2_item_3.jpg  # Tech Bundle - Wireless Charger
└── logos/           # Store logos
    ├── target.png   # Target logo
    ├── apple.png    # Apple Store logo
    ├── bestbuy.png  # Best Buy logo
    ├── gamestop.png # GameStop logo
    ├── amazon.png   # Amazon logo
    ├── walmart.png  # Walmart logo
    ├── costco.png   # Costco logo
    └── williams-sonoma.png # Williams Sonoma logo
```

## Naming Convention

### Single Items
- **Format**: `item_{id}.jpg`
- **Example**: `item_1.jpg`, `item_2.jpg`, `item_3.jpg`
- **Corresponds to**: `single_items` array in `items.json`

### Showcase Items
- **Format**: `showcase_{showcase_id}_item_{item_position}.jpg`
- **Example**: `showcase_1_item_1.jpg` (first item in first showcase)
- **Corresponds to**: Individual items within `showcases[X].items` array

### Store Logos
- **Format**: `{store_name}.png`
- **Example**: `target.png`, `apple.png`, `bestbuy.png`
- **Corresponds to**: `store.logo` field in JSON data
- **Size**: Recommend 200px wide, transparent background PNG

## Image Requirements
- **Format**: JPG preferred (PNG also works)
- **Size**: Recommend 400x300px minimum for single items, 300x200px for showcase items
- **Quality**: High enough to clearly see product details
- **Background**: Clean, preferably white or neutral

## Adding New Items
1. Add item data to `items.json`
2. Save image with corresponding filename
3. Update this README if needed
