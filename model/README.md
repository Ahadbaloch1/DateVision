# Model files

| File | In the repository? | Purpose |
|---|---|---|
| `class_names.json` | Yes | Class order (same as in training), image size (224) and the normalisation mean and standard deviation. |
| `best_model.pth` | No | Trained MobileNetV3-Large weights (`state_dict`). |

## Where to put `best_model.pth`

The weights are about 16 MB. Keep them out of the git history, because every new version of a binary file makes the repository larger.

- **For the Colab server:** upload `best_model.pth` and `class_names.json` to the Google Drive folder `Mozawati_Outputs`.
- **To share the weights publicly:** create a GitHub Release (**Releases > Draft a new release**) and attach `best_model.pth` as a release asset.

## Class order

The model output index follows `class_names.json`:

| Index | Class |
|---|---|
| 0 | Premium_Mozawati_Date |
| 1 | Semi-Ripe_Mozawati_Date |
| 2 | Ungraded_Mozawati_Date |
| 3 | Unripe_Mozawati_Date |

Do not reorder this list. It must match the order used when the model was trained.
