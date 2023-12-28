# Distrobox

# Snapshot
## via: Save / Restore
https://github.com/89luca89/distrobox/blob/main/docs/useful_tips.md#container-save-and-restore

>To save, export and reuse an already configured container, you can leverage podman save or docker save and podman import or docker import to create snapshots of your environment.
>
>with podman:
>```
>podman container commit -p distrobox_name image_name_you_choose
>podman save image_name_you_choose:latest | bzip2 > image_name_you_choose.tar.bz
>```
>Now you can backup that archive or transfer it to another host, and to restore it just run
>```
>podman load < image_name_you_choose.tar.bz2
>```
