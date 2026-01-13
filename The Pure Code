import { Ionicons } from "@expo/vector-icons";
import React, { useState } from "react";
import {
  Animated,
  ScrollView,
  StyleSheet,
  Text,
  TouchableOpacity,
  View,
} from "react-native";

export default function ExploreScreen() {
  const [imageHeight] = useState(new Animated.Value(260)); // initial height

  const expandImage = () => {
    Animated.timing(imageHeight, {
      toValue: 450, // expanded height
      duration: 300,
      useNativeDriver: false,
    }).start();
  };

  const shrinkImage = () => {
    Animated.timing(imageHeight, {
      toValue: 260, // original height
      duration: 300,
      useNativeDriver: false,
    }).start();
  };

  return (
    <ScrollView
      contentContainerStyle={{ paddingBottom: 40 }}
      style={styles.container}
    >
      {/* Hero Image with press */}
      <TouchableOpacity
        activeOpacity={0.9}
        onPressIn={expandImage}
        onPressOut={shrinkImage}
      >
        <Animated.Image
          source={{
            uri: "https://images.unsplash.com/photo-1521017432531-fbd92d768814",
          }}
          style={[styles.image, { height: imageHeight }]}
        />
      </TouchableOpacity>

      {/* Content Card */}
      <View style={styles.card}>
        {/* Title Row */}
        <View style={styles.titleRow}>
          <Text style={styles.title}>The Morning Brew</Text>

          <View style={styles.badge}>
            <Text style={styles.badgeText}>TOP RATED</Text>
          </View>
        </View>

        {/* Location */}
        <View style={styles.row}>
          <Ionicons name="location-outline" size={16} color="#FF8C00" />
          <Text style={styles.location}>San Francisco, CA · 0.8 mi away</Text>
        </View>

        {/* About */}
        <Text style={styles.sectionTitle}>ABOUT</Text>
        <Text style={styles.description}>
          {
            "Experience the perfect blend of rustic charm and modern coffee culture. Whether you're here for a quick espresso or a long afternoon of work, our calm atmosphere creates the perfect backdrop for moments that matter."
          }
        </Text>

        {/* Details */}
        <Text style={styles.sectionTitle}>DETAILS</Text>

        <View style={styles.detailBox}>
          <Ionicons name="time-outline" size={20} color="#FF8C00" />
          <View style={{ marginLeft: 8 }}>
            <Text style={styles.detailTitle}>Opening Hours</Text>
            <Text style={styles.detailText}>
              Mon - Fri, 07:00 AM - 07:00 PM
            </Text>
            <Text style={styles.open}>Open</Text>
          </View>
        </View>

        <View style={styles.detailBox}>
          <Ionicons name="call-outline" size={20} color="#FF8C00" />
          <View style={{ marginLeft: 8 }}>
            <Text style={styles.detailTitle}>Phone Number</Text>
            <Text style={styles.detailText}>+1 (415) 555-0192</Text>
          </View>
        </View>

        {/* Tags */}
        <View style={styles.tags}>
          <Text style={styles.tag}>Free WiFi</Text>
          <Text style={styles.tag}>Specialty</Text>
          <Text style={styles.tag}>Patio</Text>
        </View>

        {/* Button */}
        <TouchableOpacity style={styles.button}>
          <Text style={styles.buttonText}>Book Now →</Text>
        </TouchableOpacity>
      </View>
    </ScrollView>
  );
}

const styles = StyleSheet.create({
  container: {
    backgroundColor: "#F6F6F6",
  },
  image: {
    width: "100%",
  },
  card: {
    backgroundColor: "#fff",
    marginTop: -24,
    borderTopLeftRadius: 24,
    borderTopRightRadius: 24,
    padding: 20,
  },
  titleRow: {
    flexDirection: "row",
    justifyContent: "space-between",
    alignItems: "center",
  },
  title: {
    fontSize: 22,
    fontWeight: "700",
  },
  badge: {
    backgroundColor: "#FFF3E0",
    paddingHorizontal: 10,
    paddingVertical: 4,
    borderRadius: 12,
  },
  badgeText: {
    color: "#FF8C00",
    fontSize: 12,
    fontWeight: "600",
  },
  row: {
    flexDirection: "row",
    alignItems: "center",
    marginTop: 8,
  },
  location: {
    marginLeft: 6,
    color: "#666",
  },
  sectionTitle: {
    marginTop: 20,
    fontWeight: "600",
    color: "#999",
    fontSize: 12,
  },
  description: {
    marginTop: 8,
    lineHeight: 20,
    color: "#444",
  },
  detailBox: {
    flexDirection: "row",
    alignItems: "flex-start",
    backgroundColor: "#FAFAFA",
    padding: 14,
    borderRadius: 12,
    marginTop: 12,
  },
  detailTitle: {
    fontWeight: "600",
  },
  detailText: {
    color: "#666",
    marginTop: 2,
  },
  open: {
    color: "green",
    marginTop: 4,
    fontWeight: "600",
  },
  tags: {
    flexDirection: "row",
    marginTop: 16,
    gap: 8,
  },
  tag: {
    backgroundColor: "#F1F1F1",
    paddingHorizontal: 12,
    paddingVertical: 6,
    borderRadius: 16,
    fontSize: 12,
  },
  button: {
    backgroundColor: "#FF8C00",
    padding: 16,
    borderRadius: 12,
    alignItems: "center",
    marginTop: 24,
  },
  buttonText: {
    color: "#fff",
    fontWeight: "700",
    fontSize: 16,
  },
});
