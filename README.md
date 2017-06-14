# Notes
personal notes on coding

Enter database
docker exec -it datastore psql msm_datastore -U msm_agent


## useful notes
<span data-bind="text: $parent.func()"></span>

docker run --name datastore -p 5432:5432 -v /var/log/backup:/var/log/backup -d -it --restart=always docker.barrukka.local:5000/build/datastore

git update-index --assume-unchanged

undo commit --> git reset HEAD~  

rebase --> git reset --hard origin/develop

## CSS stuff! --->
id is #myId and class is .myClass
if you put id/class next to each other with space it will apply for any descendant. same for double arrow
without space it will apply to direct combination of the two. One arrow is a direct descendant. 
pull request 13027

^(?=([a-zA-Z0-9]*[-]*)*$)
display: inline-block or inline-flex (to align as well)
vertical-align: top (to align elements)

### css queries. 
$$("#update-plan-details")   > query with id
$$("button.btn") > query with class

$$("#update-plan-details > button") > nested query also possible

right click and copy xpath or selector

## xrandr
xrandr --query
Planning notes

stuff changes when stuff clicked in planningRenderer
loading and saving in plan.js

chromium-browser --no-proxy-server &
Config.js has all equipment config

## jquery notes
document is the HTML DOM document object model that is loaded in a web browser from html docs
events like "change" "click" are from javascript

## Pycharm notes
source can be set in project structure
bash notes
echo $?

## python notes

import traceback
traceback.print_exc()

## knockout notes
if pureComputed doesnt get triggered, try computed.

const errors = ko.validation.group([linkLength, minReceiveSignal], {deep: true, observable: true});
errors.showAllMessages()    // shows all error messages

if errors not showing on a variable due to change
var.valueHasMutated()
html notes

alert alert-danger is an alert class used in msm

