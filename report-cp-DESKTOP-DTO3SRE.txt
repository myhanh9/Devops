root@DESKTOP-DTO3SRE:/home/hanhttm# hostname=$(hostname)
root@DESKTOP-DTO3SRE:/home/hanhttm# echo "HOSTNAME: $hostname" >> report-cp-$hostname.txt
root@DESKTOP-DTO3SRE:/home/hanhttm# echo "DATE: $(date)" >> report-cp-$hostname.txt
root@DESKTOP-DTO3SRE:/home/hanhttm# echo -e "\nThong tin he thong" >> report-cp-$hostname.txt
root@DESKTOP-DTO3SRE:/home/hanhttm# echo -e "\nCPU Specs:" >> report-cp-$hostname.txt
root@DESKTOP-DTO3SRE:/home/hanhttm# echo -e "SLCPU: \n$(lscpu)" >> report-cp-$hostname.txt
root@DESKTOP-DTO3SRE:/home/hanhttm# echo -e "\nHardware Specs:" >> report-cp-$hostname.txt
root@DESKTOP-DTO3SRE:/home/hanhttm# echo -e "\nLSHW: \n$(lshw)" >> report-cp-$hostname.txt
root@DESKTOP-DTO3SRE:/home/hanhttm# echo -e "\nLSDEV: \n$(lsdev)" >> report-cp-$hostname.txt
root@DESKTOP-DTO3SRE:/home/hanhttm# echo -e "\nNetwork Info:" >> report-cp-$hostname.txt
root@DESKTOP-DTO3SRE:/home/hanhttm# echo -e "\nIP Address:\n$(ip addr | grep -oP 'inet\s+\K[\d.]+(?=/)')" >> report-cp-$hostname.txt
root@DESKTOP-DTO3SRE:/home/hanhttm# echo -e "\nMAC:\n$(ifconfig | grep ether | awk '{print $2}')" >> report-cp-$hostname.txt
