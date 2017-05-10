#!/bin/sh

service=name_of_service

PIDS=`ps -ef | grep $service | grep -v grep | awk '{print $2}'`

if [ -z "$PIDS" ]; then
  start_your_service_here
  echo "$service $USER is started." 1>&2
  exit 1
else
  for PID in $PIDS; do
    echo "$service $USER already running on PID $PIDS."
  done
fi
