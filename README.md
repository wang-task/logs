# logs

### 使用

' ' '

              export CURRENT_TIME=_修改_这里_$(date +"%Y-%m-%d_%H-%M-%S")
              __修改__这里__ | tee >> "${CURRENT_TIME}.log"
              git clone https://github.com/wang-task/logs.git
              mv ./"${CURRENT_TIME}.log" ./logs/__修改__
              echo "| [${CURRENT_TIME}.log](./${CURRENT_TIME}.log) |" >> ./logs/__这里__/index.md
              cd logs
              git config --local user.email "41898282+github-actions[bot]@users.noreply.github.com"
              git config --local user.name "github-actions[bot]"
              git add .
              git commit -a  -m "机器人🤖-运行日志_"
    - name: Push changes
      uses: ad-m/github-push-action@master
      with:
        github_token: ${{ secrets.TOKEN }}
        branch: main
        repository: 'wang-task/logs'
        directory: './logs'

' ' '
