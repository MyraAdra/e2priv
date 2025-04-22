# E2PRIV

First follow the instructions for [installing E2VID](https://github.com/uzh-rpg/rpg_e2vid).

## Run

- Download the E2PRIV pretrained model:

```bash
https://www.dropbox.com/scl/fi/sb5ddg2rfbxjiea91dex4/e2priv_pretrained_weights.pt?rlkey=588foykyo9r4qwvvmjhxpk202&st=fmvjngvh&dl=0
```

- Download an example file with event data:

```bash
wget "http://rpg.ifi.uzh.ch/data/E2VID/datasets/ECD_IJRR17/dynamic_6dof.zip" -O data/dynamic_6dof.zip
```

- Run reconstruction:

```bash
python run_reconstruction.py \
  -c pretrained/checkpoint_bbox_FULL_epoch_3.pt \
  -i data/dynamic_6dof.zip \
  --auto_hdr \
  --display \
  --show_events


## Re-training E2VID for Anonymization

- Run the Training_e2priv notebook
